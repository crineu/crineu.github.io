# Henriquinho | __<span id="id_age_mcqueen"></span>__

> <span id="id_bday_mcqueen"></span>

Tinha a idade do mano mais ou menos em __<span id="id_past_mcqueen"></span>__


---


# Eduardinho | __<span id="id_age_bolinha"></span>__

> <span id="id_bday_bolinha"></span>

<span id="id_age_diff"></span> mais novo.

Vai ter a idade do mano aproximadamente em __<span id="id_futu_bolinha"></span>__


<script src="/moment.min.js"></script>
<script src="/moment.pt-br.js"></script>

<script type="text/javascript">
    var moment_mcqueen = moment('2013-08-26 09:02 -0300', 'YYYY-MM-DD HH:mm Z');
    var moment_bolinha = moment('2016-12-01 18:05 -0300', 'YYYY-MM-DD HH:mm Z');

    var dur_age_diff = moment.duration(moment_bolinha.diff(moment_mcqueen));

    var dur_age_mcqueen = moment.duration(moment().diff(moment_mcqueen));
    var dur_age_bolinha = moment.duration(moment().diff(moment_bolinha));

    var moment_past_mcqueen = moment_mcqueen.clone().add(dur_age_bolinha);
    var moment_futu_bolinha = moment_bolinha.clone().add(dur_age_mcqueen);

    document.getElementById("id_bday_mcqueen").innerHTML = moment_mcqueen.format('LL');
    document.getElementById("id_bday_bolinha").innerHTML = moment_bolinha.format('LL');

    document.getElementById("id_age_diff").innerHTML = dur2string(dur_age_diff);

    document.getElementById("id_age_mcqueen").innerHTML = dur2string(dur_age_mcqueen);
    document.getElementById("id_age_bolinha").innerHTML = dur2string(dur_age_bolinha);

    document.getElementById("id_past_mcqueen").innerHTML = moment_past_mcqueen.format('LL');
    document.getElementById("id_futu_bolinha").innerHTML = moment_futu_bolinha.format('LL');

    function dur2string(duration) {
        var text = "";
        if (duration.years() > 0) {
            text += duration.years() + " anos, ";
        }
        if (duration.months() > 0) {
            text += duration.months() + " meses, ";
        }
        return  text + duration.days() + " dias e " + duration.hours() + " horas";
    }

</script>

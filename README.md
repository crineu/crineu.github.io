# Henriquinho | __<span id="id_age_mcqueen"></span>__

> <span id="id_bday_mcqueen"></span>

Próxima translação terrestre em __<span id="id_next_mcqueen"></span>__.

Tinha a idade do mano mais ou menos em __<span id="id_past_mcqueen"></span>__

---


# Eduardinho | __<span id="id_age_bolinha"></span>__

> <span id="id_bday_bolinha"></span>

<span id="id_age_diff"></span> mais novo.

Próxima translação terrestre em __<span id="id_next_bolinha"></span>__.

Terá a idade do mano ali por __<span id="id_futu_bolinha"></span>__


<script src="/moment.min.js"></script>
<script src="/moment.pt-br.js"></script>

<script type="text/javascript">
    // mo_* represents a 'moment'   = point in time
    // du_* represents a 'duration' = time interval

    var mo_mcqueen = moment('2013-08-26 09:02 -0300', 'YYYY-MM-DD HH:mm Z');
    var mo_bolinha = moment('2016-12-01 18:05 -0300', 'YYYY-MM-DD HH:mm Z');

    var du_age_diff = moment.duration(mo_bolinha.diff(mo_mcqueen));

    var du_age_mcqueen = moment.duration(moment().diff(mo_mcqueen));
    var du_age_bolinha = moment.duration(moment().diff(mo_bolinha));

    var mo_next_mcqueen = mo_mcqueen.clone().add(du_age_mcqueen.years() + 1, 'years');
    var mo_next_bolinha = mo_bolinha.clone().add(du_age_bolinha.years() + 1, 'years');

    var mo_past_mcqueen = mo_mcqueen.clone().add(du_age_bolinha);
    var mo_futu_bolinha = mo_bolinha.clone().add(du_age_mcqueen);


    document.getElementById("id_bday_mcqueen").innerHTML = mo_mcqueen.format('LL');
    document.getElementById("id_bday_bolinha").innerHTML = mo_bolinha.format('LL');

    document.getElementById("id_age_diff").innerHTML = du_to_str(du_age_diff);

    document.getElementById("id_age_mcqueen").innerHTML = du_to_str(du_age_mcqueen);
    document.getElementById("id_age_bolinha").innerHTML = du_to_str(du_age_bolinha);

    document.getElementById("id_next_mcqueen").innerHTML = du_to_str(moment.duration(mo_next_mcqueen.diff(moment())));
    document.getElementById("id_next_bolinha").innerHTML = du_to_str(moment.duration(mo_next_bolinha.diff(moment())));

    document.getElementById("id_past_mcqueen").innerHTML = mo_past_mcqueen.format('LL');
    document.getElementById("id_futu_bolinha").innerHTML = mo_futu_bolinha.format('LL');

    function du_to_str(duration) {
        var years  = duration.years();
        var months = duration.months();
        var days   = duration.days();
        var hours  = duration.hours();
        var text = "";

        if (years > 0) {
            text += years + (years == 1 ? " ano, " : " anos, ");
        }
        if (months > 0) {
            text += months + (months == 1 ? " mês, " : " meses, ");
        }

        text += days + (days == 1 ? " dia e " : " dias e ");
        text += hours + (hours == 1 ? " hora" : " horas");
        return text;
    }

</script>

# Henriquinho | __<span id="idadeHenrique"></span>__

> <span id="birthdayHenrique"></span>

Tinha a idade do mano em __<span id="passadoHenrique"></span>__


---


# Eduardinho | __<span id="idadeEduardo"></span>__

> <span id="birthDayEduardo"></span>
>
>
> <span id="diferencaIdade"></span> mais novo.

Vai ter a idade do mano em __<span id="futuroEduardo"></span>__


<script src="/moment.min.js"></script>
<script src="/moment.pt-br.js"></script>

<script type="text/javascript">
    var nascimentoHenrique = moment('20130826');
    var nascimentoEduardo  = moment('20161201');

    var diferencaIdade = moment.duration(nascimentoEduardo.diff(nascimentoHenrique));

    var idadeHenrique = moment.duration(moment().diff(nascimentoHenrique));
    var idadeEduardo  = moment.duration(moment().diff(nascimentoEduardo));

    var passadoHenrique = nascimentoHenrique.clone().add(idadeEduardo);
    var futuroEduardo   = nascimentoEduardo.clone().add(idadeHenrique);

    document.getElementById("birthdayHenrique").innerHTML = nascimentoHenrique.format('LL');
    document.getElementById("birthDayEduardo").innerHTML  = nascimentoEduardo.format('LL');

    document.getElementById("diferencaIdade").innerHTML = durationToString(diferencaIdade);

    document.getElementById("idadeHenrique").innerHTML = durationToString(idadeHenrique);
    document.getElementById("idadeEduardo").innerHTML  = durationToString(idadeEduardo);

    document.getElementById("passadoHenrique").innerHTML = passadoHenrique.format('LL');
    document.getElementById("futuroEduardo").innerHTML = futuroEduardo.format('LL');

    function durationToString(duration) {
        var text = "";
        if (duration.years() > 0) {
            text += duration.years() + " anos, ";
        }
        if (duration.months() > 0) {
            text += duration.months() + " meses e ";
        }
        return  text + duration.days() + " dias";
    }

</script>

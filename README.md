# Henriquinho

> <span id="birthdayHenrique"></span>

Tem __<span id="idadeHenrique"></span>__

# Eduardinho

> <span id="birthDayEduardo"></span>

Tem __<span id="idadeEduardo"></span>__


# Geometria analítica

Henriquinho tinha a idade de Eduardinho em __<span id="dataHenrique"></span>__ (há <span id="tempoPassado"></span> dias).


<script src="/moment.min.js">
</script>

<script type="text/javascript">
    var nascimentoHenrique = moment('20130826');
    var nascimentoEduardo  = moment('20161201');

    var idadeEduardo = moment.duration(moment().diff(nascimentoEduardo));
    var idadeHenrique = moment.duration(moment().diff(nascimentoHenrique));

    var dataHenriqueMesmaIdade = nascimentoHenrique.clone().add(idadeEduardo);


    document.getElementById("birthdayHenrique").innerHTML = nascimentoHenrique.format('LL');
    document.getElementById("birthDayEduardo").innerHTML  = nascimentoEduardo.format('LL');
    document.getElementById("idadeHenrique").innerHTML = durationToString(idadeHenrique);
    document.getElementById("idadeEduardo").innerHTML  = durationToString(idadeEduardo);

    document.getElementById("dataHenrique").innerHTML = dataHenriqueMesmaIdade.format('LL');
    document.getElementById("tempoPassado").innerHTML = moment().diff(dataHenriqueMesmaIdade, 'days');

    function durationToString(duration) {
        return duration.years() + " anos, " + duration.months() + " meses e " + duration.days() + " dias"
    }

</script>

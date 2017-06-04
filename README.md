## idades!

Nosso amigo Henriquinho nasceu em <span id="birthdayHenrique"></span>.

Nosso amigo Eduard nasceu em <span id="birthDayEduardo"></span>

Hoje Eduardinho tem <span id="idadeEduardo"></span>, a mesma idade que Henriquinho tinha em <span id="dataHenrique"></span> (há <span id="tempoPassado"></span> dias).

Fascinante.


<div id="para1"></div>

<script src="/moment.min.js"></script>
<script type="text/javascript">
    var nascimentoHenrique = moment('20130826');
    var nascimentoEduardo  = moment('20161201');

    document.getElementById("birthdayHenrique").innerHTML = nascimentoHenrique.format('LL');
    document.getElementById("birthDayEduardo").innerHTML = nascimentoEduardo.format('LL');

    var diasVidaEduardo = moment().diff(nascimentoEduardo, 'days');
    var dataHenriqueMesmaIdade = nascimentoHenrique.add(diasVidaEduardo, 'days');

    document.getElementById("idadeEduardo").innerHTML = nascimentoEduardo.fromNow(true);
    document.getElementById("dataHenrique").innerHTML = dataHenriqueMesmaIdade.format('LL');
    document.getElementById("tempoPassado").innerHTML = moment().diff(dataHenriqueMesmaIdade, 'days');

</script>

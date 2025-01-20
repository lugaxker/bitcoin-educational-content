---
term: BIP9

---
Método de ativação de soft forks na Bitcoin proposto em 2015. Introduz um sistema em que os mineiros sinalizam o seu apoio a um soft fork utilizando um bit específico no campo de versão dos blocos. Um soft fork proposto no âmbito do BIP9 é ativado se 95% dos blocos durante um período de 2016 blocos (aproximadamente duas semanas, coincidindo com cada ajuste de dificuldade) sinalizarem a sua aprovação. Após este bloqueio, é dado um período de tolerância para que os mineiros se preparem para a atualização antes da sua ativação. Se o limiar de 95% não for atingido no prazo máximo previsto, o soft fork é abandonado. O BIP9 permite a sinalização de vários soft forks em simultâneo, mas dá um poder considerável aos mineiros, uma vez que, se o limiar exigido não for atingido, o soft fork é simplesmente abandonado. Este método foi inicialmente utilizado para o SegWit, antes de o BIP148, que sugere a utilização de um UASF, entrar em ação e forçar o lock-in através do BIP91.
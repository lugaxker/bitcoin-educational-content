---
term: ANCHOR OUTPUTS

---
Návrh zaměřený na zlepšení správy transakčních poplatků v rámci kanálů Blesk. Při každé změně stavu v kanálu Lightning zúčastněné strany vytvoří a podepíší novou transakci závazku, která odráží nové rozdělení prostředků v rámci kanálu. Problém tohoto mechanismu spočívá v určení poplatků za transakci v okamžiku jejího vytvoření. Transakční poplatky v síti Bitcoin totiž podléhají značným výkyvům, a to jak směrem nahoru, tak dolů. Pokud jsou poplatky stanovené pro poslední závazkovou transakci v době jednostranného uzavření kanálu nedostatečné, nejenže potvrzení transakce trvá značně dlouho, ale časové zamykací mechanismy (timelocks) by také mohly umožnit krádež prostředků. Kotevní výstupy rezervují malou část prostředků v závazkové transakci na pokrytí budoucích poplatků. V případě přetížení sítě a rostoucích poplatků umožňují kotevní výstupy upravit poplatky za transakci po vytvoření závazkové transakce, a zajistit tak dostatečně rychlé uzavření kanálu Lightning.
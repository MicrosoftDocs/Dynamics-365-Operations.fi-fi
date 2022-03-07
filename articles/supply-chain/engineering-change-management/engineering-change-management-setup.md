---
title: Suunnittelun muutostenhallinnan yhteisten arvojen luominen
description: Tässä aiheessa käsitellään suunnittelun muutostenhallinnan eri osissa parametreina käytettävien yhteisten arvojen luontia.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c2ff21490dc71859d75923dd757e264096d4fcba
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565924"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Suunnittelun muutostenhallinnan yhteisten arvojen luominen

[!include [banner](../includes/banner.md)]

Suunnittelun muutostenhallinnan määrityksen yhteydessä on luotava useita arvokokoelmia, joita käytetään käyttöliittymän muissa osissa olevien avattavien luetteloiden täyttämiseen. Nämä arvot on määritettävä tuotettavien tuotetyyppien ja liiketoimintakohtaisten tarpeiden mukaan.

## <a name="engineering-change-categories"></a>Suunnittelumuutosten luokat

Suunnittelun muutosluokkien avulla suunnittelun muutostilaukset voidaan järjestää siten, että niiden hallinta ja tarkastelu helpottuu. Kätevää voi olla esimerkiksi määrittää työnkulku, jossa luokan mukaan tietyn osaston on tarkistettava ehdotetut muutokset. Tämän vuoksi suunnittelun muutostilauksessa on **Luokka**-kenttä.

Yrityksessä käytettävä suunnittelun muutosluokkien kokoelma luodaan valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinta \> Suunnittelun muutosluokat**. Toimintoruudun painikkeilla voi sitten lisätä, poistaa ja muokata arvoja sekä järjestää ne siihen järjestykseen, jossa ne näkyvät avattavissa luetteloissa.

## <a name="engineering-change-priorities"></a>Suunnittelumuutosten prioriteetit

Suunnittelun muutosten prioriteettien avulla voidaan ilmaista suunnittelun muutostilauksen tärkeys tai kiireellisyys. Ne auttavat seuraamaan suunnittelun muutostilauksen tärkeyttä, joten niiden perusteella on helppo määrittää, mitkä tilaukset on käsiteltävä ensimmäiseksi ja kuinka nopeasti ne on käsiteltävä.

Yrityksessä käytettävä suunnittelun muutosten prioriteettien kokoelma luodaan valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinta \> Suunnittelun muutosten prioriteetit**. Toimintoruudun painikkeilla voi sitten lisätä, poistaa ja muokata arvoja sekä järjestää ne siihen järjestykseen, jossa ne näkyvät avattavissa luetteloissa.

## <a name="engineering-change-reasons"></a>Suunnittelun muutoksen syyt

Suunnittelun muutoksen syyt ilmaisevat, mikä on muutostilauksen muutoksen syy tai sen luonne.

Yrityksessä käytettävä suunnittelun muutosten syykokoelma luodaan valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinta \> Suunnittelun muutosten syyt**. Toimintoruudun painikkeilla voi sitten lisätä, poistaa ja muokata arvoja sekä järjestää ne siihen järjestykseen, jossa ne näkyvät avattavissa luetteloissa.

## <a name="material-disposal-codes"></a>Materiaalin poistokoodit

Materiaalin poistokoodien avulla voi luokitella materiaalit, joita käytetään valmiissa tuotteissa, tai osat, jotka on hävitettävä tietyllä tavalla tai joita on käsiteltävä, ennen kuin ne voidaan lisätä muiden jätteiden joukkoon. Kun suunnittelun muutostilaukseen lisätään tuote, poistokoodi voidaan määrittää muutostietojen osana.

Yrityksessä käytettävä materiaalien poistokoodien kokoelma luodaan valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinta \> Materiaalien poistokoodit**. Toimintoruudun painikkeilla voi sitten lisätä, poistaa ja muokata arvoja sekä järjestää ne siihen järjestykseen, jossa ne näkyvät avattavissa luetteloissa.

## <a name="received-customer-approval"></a>Asiakkaan hyväksyntä saatu

Kun tuotteita suunnitellaan tietylle asiakkaalle, suunnittelu ja tekniset tiedot on usein vahvistettava, ennen kuin tuote voidaan määrittää valmiiksi. **Asiakkaan hyväksyntä saatu** -kentän avulla voidaan ilmaista, missä asiakkaan hyväksyntäprosessin vaiheessa tuote on ja/tai onko hyväksyntä saatu.

Yrityksessä käytettävä asiakkaalta saatujen hyväksynnän arvojen kokoelma luodaan valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinta \> Asiakkaan hyväksyntä saatu**. Toimintoruudun painikkeilla voi sitten lisätä, poistaa ja muokata arvoja sekä järjestää ne siihen järjestykseen, jossa ne näkyvät avattavissa luetteloissa.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Suunnittelun muutos – ympäristön terveellisyys- ja turvallisuuskoodit

Jos tuotteen valmistuksessa on otettava huomioon yleisiä ympäristöterveys- ja turvallisuussääntöjä tai yrityskohtaisia määräyksiä tai toimenpiteitä, ne voidaan määrittää ympäristön terveellisyys- ja turvallisuuskoodien avulla. Suunnittelun muutostilauksessa voidaan ilmaista tuotteen valmistuksessa käytettävät koodit, kun tällaisen tuotteen tietoja muokataan.

Yrityksessä käytettävä terveys- ja turvallisuusarvojen kokoelma luodaan valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinta \> Suunnittelun muutos – ympäristön terveellisyys- ja turvallisuuskoodit**. Toimintoruudun painikkeilla voi sitten lisätä, poistaa ja muokata arvoja sekä järjestää ne siihen järjestykseen, jossa ne näkyvät avattavissa luetteloissa.

## <a name="engineering-change-severities"></a>Suunnittelumuutosten vakavuudet

Suunnitellun muutosten vakavuusasteella ilmaistaan vaikutuksen taso, joka koskee suunnittelun muutostilauksessa olevia tuotteita.

Yrityksessä käytettävä suunnittelun muutosten vakavuusasteiden kokoelma luodaan valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinta \> Suunnittelun muutosten vakavuusasteet**. Toimintoruudun painikkeilla voi sitten lisätä, poistaa ja muokata arvoja sekä järjestää ne siihen järjestykseen, jossa ne näkyvät avattavissa luetteloissa.

Voit luoda säännöt, joita käytetään kullakin luotavalle vakavuustasolla. Lisätietoja näiden sääntöjen määrittämisestä on seuraavassa osassa.

## <a name="engineering-change-severity-rule-sets"></a>Suunnittelumuutosten vakavuussääntöjoukot

Suunnittelun muutosten vakavuussääntöjen joukkojen avulla voi luoda sääntöryhmiä, joilla voi laskea automaattisesti muutostilauksen vakavuusasteen tuotteissa tehtävien muutosten tyyppien perusteella. Vakavuussääntöjä käytetään avaamalla **Suunnittelun muutostenhallinnan parametrit** -sivu ja määrittämällä **Vakavuussääntö** -kentän asetukseksi *Laske* tai *Laske automaattisesti*.

Kun järjestelmä arvioi vakavuusasteen, se käsittelee säännöt ylhäältä alaspäin siinä järjestyksessä, jossa ne ovat sivulla. Säännön valitseminen ja sen prioriteetin muodostaminen edellyttää, että kaikki säännön säännöt toteutuvat.

Voit määrittää säännöt, joita käytetään jokaisessa määritetyssä muutoksen vakavuusasteessa, valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinta \> Suunnittelun muutosten vakavuussääntöjoukot**. Tee sitten jokin seuraavista:

- Luo uusi sääntöjoukko valitsemalla toimintoruudussa **Uusi** ja määritä sitten kentät myöhemmin tässä osassa kuvatulla tavalla.
- Muokkaa aiemmin luotua sääntöjoukkoa valitsemalla se luetteloruudussa ja valitsemalla sitten toimintoruudussa **Muokkaa**. Määritä sitten kentät jäljempänä tässä osassa kuvatulla tavalla.
- Poista aiemmin luotu sääntöjoukko valitsemalla se luetteloruudussa ja valitsemalla sitten toimintoruudussa **Poista**.
- Järjestä sääntöjoukkojen luettelo uudelleen valitsemalla sääntöjoukko luetteloruudussa ja sijoittamalla se uudelleen toimintoruudun **Ylös**- ja **Alas**-painikkeilla.

Määritä seuraava kenttä kullekin sääntöjoukolle:

- **Vakavuusaste** – Valitse vakavuusaste, jolle säännöt luodaan. Tasot luodaan ja nimetään **Suunnittelun muutosten vakavuusasteet** -sivulla. (Lisätietoja on edellisessä osassa.)

Lisää tai poista valittuna olevan vakavuusasteen sääntöjä **Säännöt**-pikavälilehden painikkeilla. Kullakin säännöllä on **Sääntö**- ja **Nimi**-kenttä. Järjestelmä luo nämä säännöt, ja ne ilmaisevat muutostyypit, joita tuotteella voi olla. Nimi ilmaisee muutoksen tyypin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
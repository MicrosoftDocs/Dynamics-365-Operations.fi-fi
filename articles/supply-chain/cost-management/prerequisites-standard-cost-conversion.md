---
title: Standardikustannuksen muuntamisen edellytykset
description: Tässä ohjeaiheessa käsitellään tehtäviä, jotka on suoritettava ennen standardikustannusten muuntoa.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b78cfb2c6f0462a86cf3785038c5fe4e5d63b9cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809683"
---
# <a name="prerequisites-for-a-standard-cost-conversion"></a>Standardikustannuksen muuntamisen edellytykset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään tehtäviä, jotka on suoritettava ennen standardikustannusten muuntoa. 

Toimi ennen standardikustannusten muuntoa seuraavasti:

1.  Määritä standardikustannuksille **nimikemalliryhmä**. Nimikemalliryhmät-sivulla voit luoda nimikemalliryhmän, joka käyttää standardikustannusvarastomallia. Kun määrität standardikustannusten muuntoa, määritä tämä nimikemalliryhmä muunnettaville nimikkeille.
2.  Määritä jokaiselle nimikkeelle **kustannusryhmä**.
    -   Ostetulle nimikkeelle määritetty kustannusryhmä voi toimia perustana määritettäessä kirjanpitotilejä, jotka liittyvät standardikustannuksiin. Tällöin kirjanpitotilejä voidaan määrittää esimerkiksi ostohinnan variansseille. Tuotantoympäristössä ostetuille komponenteille määritetyn kustannusryhmänavulla voi ryhmitellä valmistetun nimikkeen lasketut kustannukset.
    -   Valmistetulle nimikkeelle määritetty kustannusryhmä voi toimia perustana määritettäessä kirjanpitotilejä, jotka liittyvät standardikustannuksiin, esimerkiksi määritettäessä kirjanpitotilejä tuotannon variansseille.

3.  Määritä valmistetun nimikkeen **vakiotilausmäärä**, jos nimikkeellä on vakiokustannukset. Valmistetun nimikkeen vakiotilausmäärä toimii kirjanpidollisena eräkokona vakiokustannusten kuoletuksessa tai suhteellisessa jakamisessa. Näitä voivat olla reititystyövaiheiden asetusajat tai tuoterakenteen komponenttien vakiomäärä.
4.  Määritä standardikustannuksiin ja erityisesti uudelleenarvioinnin varianssiin liittyvät **kirjanpitotilit**. **Kirjaus**-sivulla (**Varastonhallinta** &gt; **Asetukset**) voit määrittää kirjanpitotilit, jotka liittyvät standardikustannuksiin. Standardikustannusten muuntoprosessissa on vähintään määritettävä kaikkien nimikkeiden ja kustannusryhmien uudelleenarvioinnin varianssin kirjanpitotili. **Tilikartta**-sivulla voit määrittää standardikustannuksissa tarvittavat kirjanpitotilit. **Tapahtumayhdistelmät**-sivulla voit ottaa käyttöön kustannussuhteet (taulukoissa, ryhmissä ja kaikissa kohteissa) ennen nimikekirjaussääntöjen määrittämistä.
5.  Määritä standardikustannuksiin liittyvät varastoparametrit. **Varasto ja varastonhallinnan parametrit** -sivun **Numerosarjat**-välilehdessä voit määrittää uudelleenarvostustositteiden numerojärjestyksen. Uudelleenarvostustosite luodaan, kun standardikustannusten muunnon tulos poikkeaa nimikkeen varastoarvosta. **Varasto ja varastonhallinnan parametrit** -sivulla voit määrittää kaksi standardikustannuksiin liittyvää parametria määrittämällä kustannusseurantaparametrit (**Varastokirjanpito**-välilehdessä).
    -   **Kustannuserittely**-kentässä voit valita arvoksi Ei tai Alakirjanpito. Alakirjanpito-valintaa kutsutaan aktiiviseksi kustannuserittelyksi. Aktiivista kustannuserittelyä tarvitaan, kun kustannusryhmien segmentointi lasketaan, säilytetään ja otetaan tarkasteluun monitasoisessa tuoterakenteessa standardikustannusnimikkeitä varten. Kun kustannuserittely on aktiivinen, voit raportoida ja analysoida seuraavat tiedot yksi- tai monitasoisessa tai kokonaisessa muodossa:
        1.  Varasto
        2.  Keskeneräiset työt
        3.  Myytyjen tuotteiden kustannukset kustannusryhmää kohti

        Aktiivinen kustannuserittely tarkoittaa sitä, että valmistetun nimikkeen kustannuksen käyttöönotto aiheuttaa kustannusryhmän segmentoinnin tallentamisen nimikkeen kustannustietoihin. Jos **Kustannuserittely**-kenttään ei syötetä mitään arvoa, kustannusryhmän segmentointia ei ylläpidetä standardikustannusnimikkeissä. Tämä merkitsee, että valmistetun nimikkeen standardikustannukset lasketaan ja niitä ylläpidetään yksittäisenä summana ilman kustannusryhmän segmentointia ja valmistettujen osien kustannusten osuus yhdistetään yksittäiseen summaan.
    -   **Vakio-varianssit**-kentässä voit valita yhteenvedon tai tiedot kustannusryhmittäin. Jos valitset kustannusryhmäkohtaiset tiedot, voit tunnistaa ostohinnan varianssit ja tuotannon varianssit kustannusryhmittäin. Näin voit myös määrittää neljäntyyppisiä tuotannon varianssit (erän koon, määrän, hinnan ja korvauksen varianssi). Jos valitset yhteenvedon, et voi määrittää variansseja kustannusryhmittäin etkä tunnistaa tuotannon varianssien neljää tyyppiä. Voit tarkastella vain tuotannon varianssien yhteenvetoa. Vakiovarianssia koskeva käytäntö ei riipu kustannuserittelykäytännöstä. Voit siis valita kustannuserittelykäytännöksi Ei mitään ja varianssit kustannusryhmittäin niin, että tuotannon varianssit kerätään silti kustannusryhmittäin.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
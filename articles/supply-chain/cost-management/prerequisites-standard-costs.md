---
title: Standardikustannusten edellytykset – yleiskatsaus
description: Tässä ohjeaiheessa käsitellään standardikustannusten käyttämiseen liittyvät perusvaiheet.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee676afbde465c1abb4fe4ae94e9f162f695d994
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263467"
---
# <a name="prerequisites-for-standard-costs-overview"></a>Standardikustannusten edellytykset – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään standardikustannusten käyttämiseen liittyvät perusvaiheet. Sen jälkeen vaiheet määräytyvät yrityksen työvaiheiden mukaan. Vaiheet ovat esimerkiksi erilaiset muussa kuin valmistusympäristössä, valmistusympäristössä ilman työvaiheistuksia ja valmistusympäristössä, jossa käytetään työvaiheistuksia. 

Voit määrittää standardikustannukset seuraavien ohjeiden mukaisesti.

**1. Luo nimikemalliryhmä standardikustannuksia varten.**

Luo **Nimikemalliryhmät** -sivulla uusi standardikustannusten ryhmä ja määritä **Standardikustannus**-varastomalli. Nimikkeen malliryhmän tunnuksen on oltava kuvaileva, kuten **Std-kustannus**. Valitse valintaruudut ilmaisemaan, että ryhmä sallii negatiivisen kirjanpitovaraston ja että sen on kirjattava varastotilanne ja kirjanpitovarasto. Tämä standardikustannusryhmä määritetään nimikkeille.

**2. Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit.** 

Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit **Tilikartta**-sivulla. Nämä kirjanpitotilit täytyy määrittää, ennen kuin ne voi määrittää **Kirjaus**-sivulla. Kirjanpitotilit voivat kuvastaa nimikeryhmiä ja kustannusryhmiä.

**3. Määritä standardikustannusvariansseihin liittyvät tilit varastokirjauksiin.** 

Määritä standardikustannusvariansseihin liittyvät kirjanpitotilit **Kirjaus**-sivulla. Voit määrittää varianssin kirjanpitotilin nimikkeen (tai nimikeryhmän) ja kustannusryhmän (tai kustannusryhmän tyypin) mukaan. Vaihtoehtoisesti voit määrittää, että kirjanpitotilit koskevat kaikkia nimikkeitä ja kaikkia kustannusryhmiä. Nämä vaihtoehdot vastaavat taulukoiden, ryhmien sekä kaikkien kohteiden kustannussuhteita. 

Voit ottaa kustannussuhteet käyttöön (taulukoissa, ryhmissä ja kaikissa kohteissa) **Tapahtumayhdistelmät**-sivulla ennen nimikekirjaussääntöjen määrittämistä.

**4. Määritä standardikustannuksiin liittyvät varastoparametrit.** 

-  Määritä **Varastokirjanpitokäytänteiden järjestelmä**-sivun **Tuoterakenne**-välilehdellä kaksi standardikustannuksiin liittyvää parametria.

    -  Valitse **Kustannuserittely**-kentässä voit valita arvoksi **Ei mitään** tai **Alakirjanpito**. Jos valitset **Alakirjanpito**, kustannuserittely on *aktiivinen* kustannuserittely. Aktiivista kustannusseurantaa tarvitaan välttämättä, kun kustannusryhmien segmentointi lasketaan, säilytetään ja otetaan tarkasteluun monitasoisessa tuoterakenteessa standardikustannusnimikkeitä varten. Kun kustannuserittely on aktiivinen, voit tehdä kustannusryhmäkohtaisia analyyseja ja raportteja varastoon liittyvistä tiedoista, keskeneräisistä töistä (KET-töistä) ja myytyjen tuotteiden kustannuksista (MTKUST) yksitasoisessa ja monitasoisessa muodossa sekä summamuodossa. Kun kustannuserittely on aktiivinen, valmistetun nimikkeen kustannuksen aktivointi aiheuttaa kustannusryhmän segmentoinnin tallentamisen nimikkeen kustannustietoihin. 

    -  Jos valitset **Ei mitään**, standardikustannusnimikkeiden kustannusryhmäsegmentointia ei ylläpidetä. Toisin sanoen valmistetun nimikkeen standardikustannus lasketaan ja ylläpidetään yksittäisenä summana ilman kustannusryhmän segmentointia. Valmistettujen osien kustannusvaikutukset yhdistetään yhteen summaan.

-  Valitse **Vakio-varianssit**-kentässä **Yhteensä** tai **Kustannusryhmittäin**. Jos valitset **Kustannusryhmittäin**, voit tunnistaa ostohinnan varianssit ja tuotannon varianssit kustannusryhmittäin. Voit myös määrittää neljäntyyppisiä tuotannon variansseja: erän koon, määrän, hinnan ja korvauksen varianssi. Jos valitset **Yhteensä**, et voi määrittää variansseja kustannusryhmittäin etkä tunnistaa tuotannon varianssien neljää tyyppiä. Voit tarkastella vain tuotannon varianssien yhteenvetoa.

-  Vakiovarianssia koskeva käytäntö on erillinen kustannuserittelykäytännöstä. Voit siis toisin sanoen valita kustannuserittelykäytännöksi **Ei mitään** ja varianssit kustannusryhmittäin niin, että tuotannon varianssit kerätään silti kustannusryhmittäin.

**5. Luo kustannuslaskentaversiot standardikustannuksia varten.** 

Luo **Kustannuslaskentaversion määritys** -sivulla standardikustannuksille vähintään yksi kustannuslaskentaversio. Jokaisen kustannuslaskentaversion määritys on tehtävä **Standardikustannus**-kustannuslaskentatyypillä ja kustannustietojen sisällyttäminen on sallittava.

**6. Valmistele aiemmin luotu asiakas käyttämään standardikustannuksia.** 

Jos asiakas haluaa muuttaa aiemmin luodut nimikkeensä standardikustannusvarastomallin mukaisiksi, hänen on käytettävä **Standardikustannusmuunnot**-sivua.


<a name="related-topics"></a>Liittyvät aiheet
--------

[Standardikustannuksen muuntamisen yleiskuvaus](standard-cost-conversion-overview.md)

### <a name="blogs"></a>Blogit

#### <a name="community-blogs"></a>Yhteisöblogit

- [Suorien materiaalien standardikustannusten määrittäminen Dynamics 365 for Finance and Operationsissa](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [Vakiintuneet välittömät työkustannukset Dynamics 365 for Finance and Operationsissa](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
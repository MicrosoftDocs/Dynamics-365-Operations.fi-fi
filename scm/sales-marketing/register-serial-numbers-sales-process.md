---
title: "Sarjanumeroiden rekisteröiminen myyntiprosessissa"
description: "Tässä artikkelissa kerrotaan, kuinka voit rekisteröidä sarjanumeroita pakkausluetteloihin tai laskuihin myyntiprosessin aikana. Toiminto on hyödyllinen yrityksille, jotka haluavat kerätä sarjanumeroita ainoastaan huolto- ja takuutarkoituksessa, eikä niiden tarvitse ylläpitää sarjanumeroita varaston vastaanotoille tai otoille."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ffb567c0ba9c95d059e64e24cbe0ea53ec9f7bc9
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Sarjanumeroiden rekisteröiminen myyntiprosessissa
<a id="register-serial-numbers-in-the-sales-process" class="xliff"></a>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Tässä artikkelissa kerrotaan, kuinka voit rekisteröidä sarjanumeroita pakkausluetteloihin tai laskuihin myyntiprosessin aikana. Toiminto on hyödyllinen yrityksille, jotka haluavat kerätä sarjanumeroita ainoastaan huolto- ja takuutarkoituksessa, eikä niiden tarvitse ylläpitää sarjanumeroita varaston vastaanotoille tai otoille.

Monet yritykset haluavat kerätä sarjanumeroita ainoastaan huolto- ja takuutarkoituksessa, eikä niiden tarvitse ylläpitää sarjanumeroita varaston vastaanotoille tai otoille. Näissä tilanteissa Microsoft Dynamics 365 for Finance and Operationsissa on mahdollista rekisteröidä sarjanumerot pakkausluetteloiden tai laskujen perusteella tuotteita myytäessä. Jos tuotteet myöhemmin palautettaisiinkin, voit jäljittää kunkin tuotteen laskuun ja määrittää, oletko myynyt tuotteen, ja ovatko huolto- ja takuuvelvoitteet voimassa.
Onko tiettyjä edellytyksiä?
----------------------------

Sinun on otettava käyttöön sarjanumerot myyntiprosessille **Seurantadimensioryhmät**-sivulla valitsemalla **Aktiivinen myyntiprosessissa** -valintaruutu. Seuraavat tapahtumat tapahtuvat sitten Microsoft Dynamics 365 for Finance and Operationsissa:
-   **Sarjanumerot**-pikavälilehden **Sarjanumeroiden hallinta** -asetus valitaan. Kun tämä asetus on valittuna, sinun on rekisteröitävä pakkausluettelon tai laskun kunkin nimikkeen sarjanumero.
-   Kaikki sarjanumeroiden seurantadimensioryhmän valinnat poistetaan lukuun ottamatta **Tyhjä varasto-otto sallitaan** -asetusta. Voit valita **Tyhjä varasto-otto sallitaan** -asetuksen, jos haluat ohittaa sarjanumeroiden hallinta, jotta tuotteet voi pakata ja laskuttaa ilman sarjanumeroiden rekisteröintiä.

## Milloin rekisteröin sarjanumerot myyntiprosessin aikana?
<a id="when-do-i-register-serial-numbers-during-the-sales-process" class="xliff"></a>
Voit kirjata sarjanumerot joko myyntitilauksen pakkausluettelolle tai laskulle. Kun valmistelet laskun sarjanumeroiselle nimikkeelle, joka on lähetetty pakkausluettelon kanssa, voit valita, minkä pakkausluettelon sarjanumeroista laskutat. Rekisteröityjen sarjanumeroiden määrä ei saa ylittää toimitettujen nimikkeiden määrää. Jos olet luomassa osittaista laskua, voit valita vähemmän sarjoitettuja nimikkeitä kuin on kirjattu pakkausluetteloon. Kun tulostat pakkausluettelon tai laskun, kirjatut sarjanumerot liitetään mukaan.

## Voinko määrittää sarjanumeroita skannaamalla ne vai pitääkö ne kirjoittaa?
<a id="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them" class="xliff"></a>
Voit lukea viivakoodin tai kirjoittaa sarjanumerot käsin. Kun käytät viivakoodinlukijaa, lukutila määrittää, lisätäänkö vai poistetaanko sarjanumeroita laskun tai pakkausluettelon sarjanumeroiden luettelosta. Jos haluat tarkistaa sarjanumerot esimerkiksi kannettavalla viivakoodin lukulaitteella, määritä skanneri lähettääksesi Syötä- tai sarkainkomennon sarjanumeron jälkeen. Tämä komento ilmaisee tietovirran loppua. Muussa tapauksessa täytyy painaa Enter- tai sarkainnäppäintä kunkin sarjanumeron lukemisen jälkeen.

## Jos myyntiprosessin sarjanumerot otetaan käyttöön, pitääkö kaikille nimikkeille rekisteröidä sarjanumerot?
<a id="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items" class="xliff"></a>
Tuotteelle määritetyn seurantadimensioryhmän asetukset määrittävät, onko sarjanumerot rekisteröitävä kaikille pakkausluettelon tai laskun nimikkeille. Kun otat myyntiprosessin sarjanumerot käyttöön, **Sarjanumeroiden hallinta** -asetus valitaan automaattisesti. Sinun on sitten rekisteröitävä yksi sarjanumero tai rekisteröitävä tyhjä merkintä lukukelvottomalle numerolle, jokaiselle nimikkeelle pakkausluettelossa tai laskussa. Jos et halua edellyttää kunkin nimikkeen sarjanumeroa, valitse **Tyhjä varasto-otto sallitaan** -asetus seurantadimensioryhmässä, joka liitetään nimikkeeseen. Sitten voit rekisteröidä vähemmän sarjanumeroita, kuin lähetettävien nimikkeiden määrä. Jos sarjanumeroita rekisteröidään useampi kuin toimituksessa oleva nimikemäärä, pakkausluetteloa tai laskua ei voi kirjata.

## Voinko tallentaa sarjanumerot osittaisille laskuille ja osittaisille toimituksille?
<a id="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments" class="xliff"></a>
Voit luoda osittaisen laskun ja pakkausluettelon myyntitilauksille ja rekisteröidä vain sarjanumerot nimikkeistä, jotka kyseisiin laskuihin ja pakkausluetteloihin kuuluvat. Jos haluat luoda useamman kuin yhden osittaisen laskun ja sinulla on useita myyntitilauksen pakkausluetteloja, voit lisätä usean pakkausluettelon sarjanumerot. Pakkausluetteloita, johon kaikki sarjanumerot eivät sisälly voi kuitenkin olla vain yksi. Jos sinulla on kolme pakkausluetteloa ja kukin sisältää kaksi sarjoitettua nimikettä, et voi luoda osittaista laskua yhdelle nimikkeelle jokaisesta pakkausluettelosta.

## Mitä teen, kun sarjanumero ei ole lukukelpoinen?
<a id="what-do-i-do-when-a-serial-number-isnt-readable" class="xliff"></a>
Jos järjestysnumeroa ei voi lukea tai skannata, voit luoda tyhjän rivin nimikkeen valitsemalla **Sarjanumerot**-sivulla kohdan **Ei lukukelpoinen**. Jos sarjanumero tulee myöhemmin saataville, voit päivittää laskun tai pakkausluettelon. Lisätietoja on seuraavassa osiossa, "Voinko korjata tai muuttaa myyntitilaukselle kirjatut sarjanumerot?"

## Voinko korjata tai muuttaa myyntitilaukselle kirjatut sarjanumerot?
<a id="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order" class="xliff"></a>
Kyllä, voit korjata sarjanumerot, kun seuraavat ehdot täyttyvät:
-   **Laskut** – Voit muuttaa laskuttamattomien nimikkeiden sarjanumeroita. Samalla päivitetään myös pakkausluettelo. Jos kuitenkin myyntitilausrivi on korjattu rekisteröimällä negatiivinen määrä, et voi muuttaa myyntitilausrivin sarjanumeroja.
-   **Pakkausluettelo** – Et voi korjata sarjoitettuja nimikkeitä sisältävää pakkausluetteloriviä osittain. Sinun on palautettava rivin koko määrä. Jos pakkausluettelo on peruutettu tai korjattu, sinun ei tarvitse rekisteröidä palautettuja sarjanumeroja uudelleen, kun luot uuden pakkausluettelon samoille sarjoitetuille nimikkeille. Rekisteröityjä numeroita käytetään.

## Voinko tarkastella sarjanumeroita, jotka toimitettiin tietyllä pakkausluettelolla tai sisältyivät tiettyyn laskuun?
<a id="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice" class="xliff"></a>
Kyllä, voit suorittaa kyselyn pakkausluettelon kirjauskansioriviltä tai laskun kirjauskansioriviltä tarkastellaksesi kaikkia sarjanumeroita, jotka on sisällytetty asiakirjaan.

## Voinko tarkastella sarjoitettuja kohteita, jotka minulla on?
<a id="can-i-view-the-serialized-items-that-i-have-on-hand" class="xliff"></a>
Ei, et voi tarkastella sarjoitettuja käytettävissäsi olevia nimikkeitä, koska sarjanumeroita ei ole rekisteröity nimikkeille ennen nimikkeiden myymistä.

## Voinko sarjanumerot tallentaa todellisen painon nimikkeille?
<a id="can-i-register-serial-numbers-for-catchweight-items" class="xliff"></a>
Ei, et voi rekisteröidä myyntiprosessissa sarjanumeroita todellisen painon nimikkeille. Jos tuote on lisäksi määritetty todellisen painon nimikkeeksi, et voi määrittää tuotteelle seurantadimensioryhmää, joka on asetettu käyttämään sarjanumeroita ainoastaan myyntiprosessin aikana.
Voinko rekisteröidä sarjanumeroita vähittäismyyntipisteessä?
------------------------------------------------

Kyllä, vähittäismyyntipiste kehottaa käyttäjää lisäämään sarjanumeron, kun käyttäjä myy tuotteen, jolle on määritetty seurantadimensioryhmä, joka on asetettu käyttämään sarjanumeroita ainoastaan myyntiprosessin aikana.

## Mitä käyttöoikeusrooleja tarvitaan sarjanumeroiden rekisteröintiin myyntiprosessin aikana?
<a id="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process" class="xliff"></a>
Tämä toiminnallisuus on käytettävissä kaikille rooleille, jotka voivat ylläpitää myynnin pakkausluetteloita ja laskuja. Seuraavat velvollisuudet antavat työntekijöille mahdollisuuden korjata sarjanumeroita ja rekisteröidä tyhjiä merkintöjä sellaisille sarjanumeroille, joita ei voida lukea tai skannata:
-   Ylläpidä sarjanumeroiden korjausta
-   Ylläpidä lukukelvottomien sarjanumeroiden rekisteröintiä







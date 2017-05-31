---
title: "Sarjanumeroiden rekisteröiminen myyntiprosessissa"
description: "Tässä artikkelissa kerrotaan, kuinka voit rekisteröidä sarjanumeroita pakkausluetteloihin tai laskuihin myyntiprosessin aikana. Toiminto on hyödyllinen yrityksille, jotka haluavat kerätä sarjanumeroita ainoastaan huolto- ja takuutarkoituksessa, eikä niiden tarvitse ylläpitää sarjanumeroita varaston vastaanotoille tai otoille."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d984a6af2b48f02120ea61b385522a6400d93d4a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="register-serial-numbers-in-the-sales-process"></a>Sarjanumeroiden rekisteröiminen myyntiprosessissa

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, kuinka voit rekisteröidä sarjanumeroita pakkausluetteloihin tai laskuihin myyntiprosessin aikana. Toiminto on hyödyllinen yrityksille, jotka haluavat kerätä sarjanumeroita ainoastaan huolto- ja takuutarkoituksessa, eikä niiden tarvitse ylläpitää sarjanumeroita varaston vastaanotoille tai otoille.

Monet yritykset haluavat kerätä sarjanumeroita ainoastaan huolto- ja takuutarkoituksessa, eikä niiden tarvitse ylläpitää sarjanumeroita varaston vastaanotoille tai otoille. Näissä tilanteissa Microsoft Dynamics 365 for Operations -järjestelmän avulla on sarja numerot on mahdollista rekisteröidä pakkausluetteloiden tai laskujen perusteella tuotteita myytäessä. Jos tuotteet myöhemmin palautettaisiinkin, voit jäljittää kunkin tuotteen laskuun ja määrittää, oletko myynyt tuotteen, ja ovatko huolto- ja takuuvelvoitteet voimassa.
Onko tiettyjä edellytyksiä?
----------------------------

Sinun on otettava käyttöön sarjanumerot myyntiprosessille **Seurantadimensioryhmät**-sivulla valitsemalla **Aktiivinen myyntiprosessissa** -valintaruutu. Seuraavat tapahtumat tapahtuvat sitten Microsoft Dynamics 365 for Operations -järjestelmässä:
-   **Sarjanumerot**-pikavälilehden **Sarjanumeroiden hallinta** -asetus valitaan. Kun tämä asetus on valittuna, sinun on rekisteröitävä pakkausluettelon tai laskun kunkin nimikkeen sarjanumero.
-   Kaikki sarjanumeroiden seurantadimensioryhmän valinnat poistetaan lukuun ottamatta **Tyhjä varasto-otto sallitaan** -asetusta. Voit valita **Tyhjä varasto-otto sallitaan** -asetuksen, jos haluat ohittaa sarjanumeroiden hallinta, jotta tuotteet voi pakata ja laskuttaa ilman sarjanumeroiden rekisteröintiä.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Milloin rekisteröin sarjanumerot myyntiprosessin aikana?
Voit kirjata sarjanumerot joko myyntitilauksen pakkausluettelolle tai laskulle. Kun valmistelet laskun sarjanumeroiselle nimikkeelle, joka on lähetetty pakkausluettelon kanssa, voit valita, minkä pakkausluettelon sarjanumeroista laskutat. Rekisteröityjen sarjanumeroiden määrä ei saa ylittää toimitettujen nimikkeiden määrää. Jos olet luomassa osittaista laskua, voit valita vähemmän sarjoitettuja nimikkeitä kuin on kirjattu pakkausluetteloon. Kun tulostat pakkausluettelon tai laskun, kirjatut sarjanumerot liitetään mukaan.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Voinko määrittää sarjanumeroita skannaamalla ne vai pitääkö ne kirjoittaa?
Voit lukea viivakoodin tai kirjoittaa sarjanumerot käsin. Kun käytät viivakoodinlukijaa, lukutila määrittää, lisätäänkö vai poistetaanko sarjanumeroita laskun tai pakkausluettelon sarjanumeroiden luettelosta. Jos haluat tarkistaa sarjanumerot esimerkiksi kannettavalla viivakoodin lukulaitteella, määritä skanneri lähettääksesi Syötä- tai sarkainkomennon sarjanumeron jälkeen. Tämä komento ilmaisee tietovirran loppua. Muussa tapauksessa täytyy painaa Enter- tai sarkainnäppäintä kunkin sarjanumeron lukemisen jälkeen.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Jos myyntiprosessin sarjanumerot otetaan käyttöön, pitääkö kaikille nimikkeille rekisteröidä sarjanumerot?
Tuotteelle määritetyn seurantadimensioryhmän asetukset määrittävät, onko sarjanumerot rekisteröitävä kaikille pakkausluettelon tai laskun nimikkeille. Kun otat myyntiprosessin sarjanumerot käyttöön, **Sarjanumeroiden hallinta** -asetus valitaan automaattisesti. Sinun on sitten rekisteröitävä yksi sarjanumero tai rekisteröitävä tyhjä merkintä lukukelvottomalle numerolle, jokaiselle nimikkeelle pakkausluettelossa tai laskussa. Jos et halua edellyttää kunkin nimikkeen sarjanumeroa, valitse **Tyhjä varasto-otto sallitaan** -asetus seurantadimensioryhmässä, joka liitetään nimikkeeseen. Sitten voit rekisteröidä vähemmän sarjanumeroita, kuin lähetettävien nimikkeiden määrä. Jos sarjanumeroita rekisteröidään useampi kuin toimituksessa oleva nimikemäärä, pakkausluetteloa tai laskua ei voi kirjata.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Voinko tallentaa sarjanumerot osittaisille laskuille ja osittaisille toimituksille?
Voit luoda osittaisen laskun ja pakkausluettelon myyntitilauksille ja rekisteröidä vain sarjanumerot nimikkeistä, jotka kyseisiin laskuihin ja pakkausluetteloihin kuuluvat. Jos haluat luoda useamman kuin yhden osittaisen laskun ja sinulla on useita myyntitilauksen pakkausluetteloja, voit lisätä usean pakkausluettelon sarjanumerot. Pakkausluetteloita, johon kaikki sarjanumerot eivät sisälly voi kuitenkin olla vain yksi. Jos sinulla on kolme pakkausluetteloa ja kukin sisältää kaksi sarjoitettua nimikettä, et voi luoda osittaista laskua yhdelle nimikkeelle jokaisesta pakkausluettelosta.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Mitä teen, kun sarjanumero ei ole lukukelpoinen?
Jos järjestysnumeroa ei voi lukea tai skannata, voit luoda tyhjän rivin nimikkeen valitsemalla **Sarjanumerot**-sivulla kohdan **Ei lukukelpoinen**. Jos sarjanumero tulee myöhemmin saataville, voit päivittää laskun tai pakkausluettelon. Lisätietoja on seuraavassa osiossa, "Voinko korjata tai muuttaa myyntitilaukselle kirjatut sarjanumerot?"

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Voinko korjata tai muuttaa myyntitilaukselle kirjatut sarjanumerot?
Kyllä, voit korjata sarjanumerot, kun seuraavat ehdot täyttyvät:
-   **Laskut** – Voit muuttaa laskuttamattomien nimikkeiden sarjanumeroita. Samalla päivitetään myös pakkausluettelo. Jos kuitenkin myyntitilausrivi on korjattu rekisteröimällä negatiivinen määrä, et voi muuttaa myyntitilausrivin sarjanumeroja.
-   **Pakkausluettelo** – Et voi korjata sarjoitettuja nimikkeitä sisältävää pakkausluetteloriviä osittain. Sinun on palautettava rivin koko määrä. Jos pakkausluettelo on peruutettu tai korjattu, sinun ei tarvitse rekisteröidä palautettuja sarjanumeroja uudelleen, kun luot uuden pakkausluettelon samoille sarjoitetuille nimikkeille. Rekisteröityjä numeroita käytetään.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Voinko tarkastella sarjanumeroita, jotka toimitettiin tietyllä pakkausluettelolla tai sisältyivät tiettyyn laskuun?
Kyllä, voit suorittaa kyselyn pakkausluettelon kirjauskansioriviltä tai laskun kirjauskansioriviltä tarkastellaksesi kaikkia sarjanumeroita, jotka on sisällytetty asiakirjaan.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Voinko tarkastella sarjoitettuja kohteita, jotka minulla on?
Ei, et voi tarkastella sarjoitettuja käytettävissäsi olevia nimikkeitä, koska sarjanumeroita ei ole rekisteröity nimikkeille ennen nimikkeiden myymistä.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Voinko sarjanumerot tallentaa todellisen painon nimikkeille?
Ei, et voi rekisteröidä myyntiprosessissa sarjanumeroita todellisen painon nimikkeille. Jos tuote on lisäksi määritetty todellisen painon nimikkeeksi, et voi määrittää tuotteelle seurantadimensioryhmää, joka on asetettu käyttämään sarjanumeroita ainoastaan myyntiprosessin aikana.
Voinko rekisteröidä sarjanumeroita vähittäismyyntipisteessä?
------------------------------------------------

Kyllä, vähittäismyyntipiste kehottaa käyttäjää lisäämään sarjanumeron, kun käyttäjä myy tuotteen, jolle on määritetty seurantadimensioryhmä, joka on asetettu käyttämään sarjanumeroita ainoastaan myyntiprosessin aikana.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Mitä käyttöoikeusrooleja tarvitaan sarjanumeroiden rekisteröintiin myyntiprosessin aikana?
Tämä toiminnallisuus on käytettävissä kaikille rooleille, jotka voivat ylläpitää myynnin pakkausluetteloita ja laskuja. Seuraavat velvollisuudet antavat työntekijöille mahdollisuuden korjata sarjanumeroita ja rekisteröidä tyhjiä merkintöjä sellaisille sarjanumeroille, joita ei voida lukea tai skannata:
-   Ylläpidä sarjanumeroiden korjausta
-   Ylläpidä lukukelvottomien sarjanumeroiden rekisteröintiä







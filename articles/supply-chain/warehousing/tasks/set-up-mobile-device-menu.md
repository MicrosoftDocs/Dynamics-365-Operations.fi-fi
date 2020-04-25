---
title: Määritä mobiililaitteen valikkokohde Ostotilaus-tyypin työn valmistumiselle
description: Tässä aiheessa kuvataan, miten määrität Mobiililaite-valikkovaihtoehdon.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 905094ae4e76fadbebea1892ec20427f32e3e71d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216820"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Määritä mobiililaitteen valikkokohde Ostotilaus-tyypin työn valmistumiselle

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten määrität Mobiililaite-valikkovaihtoehdon. Tässä esimerkissä valikkovaihtoehdolla suoritetaan Ostotilaus-tyypin työ. Työn voimassaolo määritetään valikkokohteeseen liitetyn työluokan perusteella. Voit käyttää tätä opastusta USMF-yrityksen demotiedoissa. Tämän menettelyn suorittaa yleensä varastopäällikkö.


## <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto
1. Siirry kohtaan **Mobiililaitteen valikkovaihtoehdot** syöttämällä teksti hakupalkkiin.
2. Valitse **Uusi**.
3. Kirjoita arvo **Valikkovaihtoehdon nimi** -kenttään. Anna yksilöivä arvo. Voit esimerkiksi kirjoittaa `POMove`. Kirjoita arvo muistiin, sillä sitä tarvitaan myöhemmin.  
4. Kirjoita **Otsikko**-kenttään arvo. Tämä on mobiililaitteessa näkyvä otsikko. Voit esimerkiksi kirjoittaa `PO Move`.  
5. Valitse **Tila**-kentässä **Työ**.
6. Valitse **Käytä nykyistä työtä** -kentässä **Kyllä**.
    - Tällä mobiililaitteen valikkovaihtoehdolla suoritetaan aiemmin luotu työ. Niinpä arvoksi on valittava **Kyllä**.  
    - **Näytä varaston tila** -kenttä määrittää, näytetäänkö varastosaldon varaston tila mobiililaitteessa varastotyöntekijälle.  
7. Valitse **Ohjaaja**-kentässä **Järjestelmän ryhmittely**. Kun valitset arvon **Ohjaaja**-kentässä, tämän sivun **Yleiset**-osaan tulee näkyviin lisäkenttiä. Näkyvät kentät määräytyvät sen mukaan, mitä olet valinnut. Kun valitset **Järjestelmän ryhmittely** -asetuksen, kaksi uutta kenttää lisätään. Ne käsitellään seuraavaksi.  
8. Kirjoita **Järjestelmän ryhmittely** -kenttään **WorkPoolId**. Kun varastotyöntekijät avaavat tämän valikkovaihtoehdon, heitä pyydetään skannaamaan työpoolin tunnus. Käyttäjälle lähetetään kaikki työtilaukset, joilla on tämä työpoolin tunnus, sekä kaikki avoimet työtilausrivit, joissa on yksi tähän valikkovaihtoehtoon lisätty työluokka.  
9. Kirjoita **Järjestelmän ryhmittelyotsikko** -kenttään arvo. Tämä teksti näkyy mobiililaitteen käyttäjälle. Voit esimerkiksi kirjoittaa **Työpooli**.  
10. Valitse **Ohita rekisterikilpi määrityksen aikana** -kentässä **Kyllä**. Varastotyöntekijät voivat ohittaa tällä asetuksella kohderekisterikilven, kun nimikkeet on laskettu alas rekisterikilpiohjattuun sijaintiin.  
11. Valitse **Ryhmä pantu pois** -kentässä **Kyllä**.
    - Jos kaikilla työtilauksen Määritä-riveillä on sama sijainti, käyttäjä vastaanottaa kaikille riveille yhden yhdistetyn Määritä-ohjeen. 
    - Tarkistusmallin tunnus: Voit määrittää työntarkistusmallin avulla, että valikkovaihtoehdon työprosessi on keskeytettävä, jotta toisen työvaihe voidaan suorittaa. Jos tämä valikkovaihtoehto on esimerkiksi saapuvalle työlle, tarkistusmalli saattaa edellyttää, että työntekijä tarkistaa lämpötilan. Prosessin keskeytyskohta määritetään tarkistusmallissa ja se voi olla esimerkiksi työn aloitus, valmistuminen tai tilan muutos.  
12. Laajenna **Työluokat**-osa.
13. Valitse **Uusi**.
14. Kirjoita **Työluokan tunnus** -kenttään `Purchase`. Työpooli rajoittaa työn, johon valikkovaihtoehtoa voi käyttää. Tässä tapauksessa sitä käytetään avoimilla työtilausriveillä, joilla ostotyöluokan tunnus.  
15. Valitse **Tallenna**.

## <a name="set-up-work-confirmation"></a>Määritä työn vahvistus
1. Valitse **Työn vahvistusasetukset**.
2. Valitse **Työtyyppi**-kentässä **Keräilyt**.
3. Valitse **Vahvista automaattisesti** -valintaruutu. Jos työn tyyppi on Keräily, sen työohjeet vahvistetaan automaattisesti. Tätä ohjetta ei näytetä käyttäjälle.  
4. Valitse **Uusi**.
5. Valitse **Työtyyppi**-kentässä Määritä.
6. Valitse **Sijainnin vahvistus** -valintaruutu. Varastotyöntekijää pyydetään vahvistamaan skannaamalla sijainti, johon nimike on laskettu alas.  
7. Valitse **Tallenna**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Lisää valikkovaihtoehto mobiililaitteen valikkoon
1. Siirry kohtaan **Mobiililaitteen valikko** syöttämällä teksti hakupalkkiin.
2. Valitse **Muokkaa**.
3. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Nimi**-kenttää arvolla **inbound**. Haluat etsi valikon, jota käytät saapuville valikkovaihtoehdoille. USMF:ssä sen nimenä on **Saapuva**.  
4. Valitse puussa **a value**.
5. Valitse oikealle osoittava nuoli.
6. Valitse **Tallenna**.
7. Sulje sivu.

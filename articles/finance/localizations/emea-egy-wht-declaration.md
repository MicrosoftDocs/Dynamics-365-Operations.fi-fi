---
title: Egyptin ennakonpidätysilmoitus
description: Tässä aiheessa kerrotaan, miten Egyptin ennakonpidätysilmoitus konfiguroidaan ja muodostetaan.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e0d13a2de9acaa8b1c896e130b4dabb222e45dcb
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881419"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Egyptin ennakonpidätysilmoitus (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Yleiskuvaus
Tässä ohjeaiheessa on tietoja ennakonpidätysilmoituksen ja ennakonpidätysilmoituksen lomakkeiden 41 ja 11 määrittämisestä ja luomisesta yrityksille Egyptissä 

Kaikkien egyptiläisten yritysten on valmisteltava lomake 41, joka sisältää yhteenvedon kaikista paikallisilta toimittajilta ja palveluntuottajilta pidätetyistä veroista. Lomakkeen 41 lisäksi on muodostettava lomake 11, jotta voidaan eritellään kaikki ulkomaisilta toimittajilta pidätetyt verot. 

Dynamics 365 Financen **Ennakonpidätysilmoitus**-raportti sisältää seuraavat raportit:

- Ilmoituslomake nro 41
- Ilmoituslomake nro 11
    
    
## <a name="prerequisites"></a>Edellytykset
Yrityksen ensisijainen osoite on on oltava Egyptissä.
**Ominaisuuksien hallinta** -työtilassa on otettava käyttöön seuraava ominaisuus:

   - **Yleinen ennakonpidätys**

Lisätietoja uusien ominaisuuksien käyttöönotosta on kohdassa [ominaisuuksien hallinnan yleiskuvaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

1. Siirry kohtaan **Vero** >  **Asetukset** > **Parametrit** > **Kirjanpitoparametrit** ja määritä **Ennakonpidätys**-välilehden **Ota yleinen ennakonpidätys käyttöön** -asetuksen arvoksi **Kyllä**.
2. Tuo **Sähköinen raportointi** -työtilassa seuraavat sähköiset raportointimuodot tietovarastosta:

    - Ennakonpidätysilmoitus, Excel (EG)

    > [!NOTE]
    > Edellä esitetty muoto perustuu **veroilmoituksen malliin** ja käyttää **veroilmoituksen mallimääritystä**. Tämä lisäkonfiguraatio tuodaan automaattisesti.

Lisätietoja sähköisen raportoinnin konfiguraatioiden tuomisesta on kohdassa [Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Services  -palveluista](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Sähköisen raportoinnin konfiguraatioiden lataaminen

Egyptin ennakonpidätysilmoituslomakkeiden toteutus, joka perustuu sähköisen raportoinnin konfiguraatioihin. Lisätietoja konfiguroitavan raportoinnin ominaisuuksista ja käsitteistä on kohdassa [Sähköinen raportointi](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Tuotanto- ja käyttäjähyväksyntätestausympäristöille on ohjeet aiheessa [Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Services -palveluista](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Jos haluat luoda ennakonpidätysilmoitukset egyptiläisessä yrityksessä, sinun on ladattava palvelimeen seuraavat konfiguraatiot:

- Veroilmoitus model.version.82.xml tai myöhempi versio
- Veroilmoituksen mallin mapping.version.82.133.xml tai myöhempi versio
- Ennakonpidätysilmoituksen Excel (EG).version.82.21 tai myöhempi versio

Kun olet ladanut ER-konfiguraatiot Lifecycle Services (LCS) -palvelusta tai yleisestä tietovarastosta, tee seuraavat toimet.

1. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.
1. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda > Lataa XML-tiedostosta**.
1. Lataa kaikki tiedostot sen mukaan, missä järjestyksessä ne on lueteltu edellisessä luettelossa. Kun kaikki konfiguraatiot on ladattu palvelimeen, konfiguraatiopuun pitäisi näkyä Financessa.

## <a name="set-up-application-specific-parameters"></a>Sovelluskohtaisten parametrien määrittäminen

Sovelluskohtaisien parametrien vaihtoehdon avulla käyttäjät voivat määrittää kriteerit, joiden mukaan verotapahtumat luokitellaan ja lasketaan kullakin luodun raportin rivillä sen mukaan, miten **ennakonpidätysnimikeryhmä** tai muu ehto on määritetty hakumäärityksessä.

Ennakonpidätyslomake 41 sisältää erityissarakkeen, jossa ennakonpidätystapahtuma on luokiteltava veroviranomaisen **Alennuskoodityyppi**-nimisen luokituksen mukaan. Sen sijaan, että nämä uudet luokittelut sisällytettäisiin uuden viennin tietoina tapahtumien kirjaamisen yhteydessä, luokittelut määritetään kohdassa **Määritykset** > **Määritä sovelluskohtaiset parametrit** > **Määritys** esiteltyjen eri hakujen mukaan, jotta täytetään Egyptin ennakonpidätysraporttien vaatimukset. 

Seuraavan konfiguraation avulla voidaan luokitella tapahtumat ennakonpidätyslomakkeen 41 raportissa:

- **DiscountTaxTypeLookup**-> Sarake nro 18 

Seuraavia ohjeita noudattamalla voit määrittää eri hakuja, joita käytetään ennakonpidätysilmoituksen ja siihen liittyvien kirjojen raporttien luomisessa. 

1. Valitse **Sähköinen raportointi** -työtilassa **Määritykset** > **Määritys**, kun haluat määrittää säännöt, jotka määrittävät, miten tapahtumat luokitellaan ennakonpidätysilmoitusraportissa. 
2. Valitse nykyinen versio ja valitse hakunimi **Haut**-pikavälilehdistä. Esimerkiksi **DiscountTaxTypeLookup**. Tämä haku määrittää veroviranomaisen edellyttämän alennustyyppien luettelon.
3. Valitse **Ehdot**-pikavälilehdessä **Lisää** ja valitse uuden rivin **Hakutulos**-sarakkeessa liittyvä rivi, joka vastaa **sarakkeen 18** luokittelua.
4. Valitse **Ennakonpidätysnimikeryhmä**-sarakkeesta liittyvä koodi, jota käytetään luokituksen tunnistamiseen. Esimerkiksi **Sallittu alennus**.  
5. Toista vaiheet 3 ja 4 kaikille käytettävissä oleville hauille.
6. Valitse uudelleen **Lisää**, jos haluat sisällyttää lopullisen tietuerivin. Valitse sitten **Hakutulos**-sarakkeesta **Ei sovellettavissa**. 
7. Valitse jäljellä olevissa sarakkeissa **Ei tyhjä**. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Kirjanpidon parametrien määrittäminen

Voit luoda ennakonpidätysilmoituslomakkeen raportit Microsoft Excelissä, kun määrität ER-muodon **Kirjanpitoparametrit**-sivulla.

1. Siirry kohtaan **Vero** > **Asetukset** > **Kirjanpitoparametrit**.
2. Valitse **Ennakonpidätys**-välilehden **Ennakonpidätysilmoituksen muodon määritys** -kentästä **Ennakonpidätysilmoitus, Excel (EG)**. Jos jätät tämän kentän tyhjäksi, arvonlisäveron vakioraportti luodaan SSRS-muodossa.


![Ilmoituslomake](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Ennakonpidätysilmoituslomakkeiden muodostaminen
Tietyn kauden ennakonpidätyslomakkeen valmistelu- ja lähetysprosessi perustuu Tilitä ja kirjaa maksun vero -työn aikana kirjattuihin ennakonpidätystapahtumiin. Lisätietoja yleisistä ennakonpidätyksistä on kohdassa [Yleinen ennakonpidätys](../general-ledger/global-withholding-tax-overview.md).

Luo veroilmoitusraportti noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Vero** > **Ilmoitus** > **Ennakonpidätys** > **Ennakonpidätysmaksu*.
2. Valitse tilityskausi ja valitse sitten raportin aloituspäivämäärä. 
3. Syötä tapahtuman päivämäärä ja valitse **OK**.
4. Valitse näyttöön tulevassa valintaikkunassa yksi tai useampi lomaketyypeistä **Form nro 41**, **Form nro 11** tai **Ei mikään**. Jos valitset **Ei mikään**, luodaan vakioraportti. 
5. Valitse kieli. Kaikki raportit käänetään kielille **en-us** ja **ar-eg**.
6. Syötä sen pankin sivuliike ja nimi, josta veromaksu maksetaan.
7. Valitse yrityksen tyyppi ja kirjoita sitten tarkistus- ja asiakirjanumerot. 
8. Anna yksikön tyyppi. 
9. Kirjoita sen henkilön nimi, joka on rekisteröity määrittämään lomake, ja vahvista raportin luonti valitsemalla **OK**. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]

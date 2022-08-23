---
title: Pilvipohjaisen haun yleiskatsaus
description: Tässä artikkelissa on yleiskatsaus pilvipohjaisesta hausta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273663"
---
# <a name="cloud-powered-search-overview"></a>Pilvipohjaisen haun yleiskatsaus

[!include [banner](includes/banner.md)]

Tässä artikkelissa on yleiskatsaus pilvipohjaisesta hausta Microsoft Dynamics 365 Commerce -sovelluksessa.

Tuotteiden löydettävyyden avulla varmistetaan, että asiakkaat löytävät tuotteita nopeasti ja helposti selaamalla luokkia sekä tekemällä hakuja ja suodattamalla luokkia. Vähittäismyyjät pitävät tuotteiden löytämistä ensisijaisena työkaluna, jolla asiakas voi toimia eri kanavien kautta Cloud Scale Unit (CSU) -yksikön avulla. Tällaisia ovat esimerkiksi sähköinen kauppa ja myyntipiste.

Asiakkaat ovat tottuneet lähes välittömiin vastausaikoihin verkon hakukoneissa, kehittyneissä sähköisen kaupankäynnin sivustoissa, yhteisöpalvelusovelluksissa, automaattisissa ehdotuksissa hakuehdotusten syöttämisen yhteydessä, kohdistetussa siirtymisessä ja korostuksissa. Jos asiakkaat eivät löydä hakemaansa tuotetta nopeasti yhdestä sähköisen kaupankäynnin myymälästä, he siirtyvät nopeasti toiseen sähköisen kaupankäynnin myymälään.

Pilvipohjaisen tuotteen etsintätoiminto Commercessa auttaa jälleenmyyjiä lisäämään asiakkaiden pysymistä ja eri CSU-kanavien muuntomääriä.

Commercen hakukokemus on parantanut ominaisuuksia, joiden avulla jälleenmyyjät saavuttavat aiempaa paremman tuotteiden löydettävyyden. Samalla nämä ominaisuudet tarjoavat skaalautuvuutta ja suorituskykyä, jota sähköisen kaupankäynnin liikenne vaatii.

## <a name="browse-and-search"></a>Selaaminen ja hakeminen

Hakurelevanssi ja suorituskyky ovat tärkeitä tekijöitä monikanavakokemuksessa, koska tuotteen löydettävyys riippuu suureksi osaksi tiedonhaun ja sisällön navigoinnin hakutoiminnoista. Tehokas selaus- ja hakukokemus auttaa muunnon lisäämisessä.

Seuraavassa kuvassa on esimerkki tyypillisestä selaus- ja hakutoiminnosta.

![Aloitussivun haku.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Kohdistetun siirtymisen ja valinnan yhteenveto 

Kohdistettu siirtyminen auttaa asiakkaita selaamaan sisältöä helpommin, koska he voivat suodattaa termeihin linkitettyjä tarkenteita termijoukossa. Kun asiakas on valinnut ja ottanut tarkenteet käyttöön, näkyviin tulee valintojen yhteenveto. 

Kohdistetun siirtymisen avulla voi määrittää erilaisia tarkenteita eri termijoukon termeille ilman, että niille on luotava erillisiä sivuja. 

Seuraavassa kuvassa on esimerkki kohdistetun siirtymisen käytöstä haussa.

![Valinnan yhteenveto.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Mukaansatempaava automaattinen ehdotustoiminto

Nykyinen automaattisen ehdotuksen toiminto näyttää avainsanat, jotka käynnistävät vastaavan avainsanan haun. Commercen uusien parannusten avulla asiakkaat voivat usein löytää linkkejä tuotteisiin ennen kuin he ovat kirjoittaneet hakusanoja.

Commerce tukee myös eri luokkiin kuuluvien avainsanavastaavuuksien toimintoja. Tämän toiminnon avulla asiakkaan näkevät vastaavien avainsanojen määrän eri luokissa. He voivat myös käynnistää avainsanahaun muissa luokissa.

Seuraavassa kuvassa näkyy esimerkki, jossa käytetään mukaansatempaavaa automaattista ehdotustoimintoa.

![Mukaansatempaava automaattinen ehdotustoiminto.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Lajittele

Lajittelutoiminnon avulla asiakkaat voivat lajitella, hakea ja selata luokan tuloksia ja tarkentaa niitä erilaisten ehtojen, kuten hinnan, tuotenimen ja tuotenumeron avulla. Jos otat [tuotesuositukset](product-recommendations.md) käyttöön ympäristössäsi, asiakkaat voivat lajitella tulokset myös lajittelun lisäkriteereiden perusteella, kuten uusi, parhaiten myyvä ja suosittu.


> [!NOTE]
> Nämä pilvipohjaiset hakutoiminnot ovat saatavilla versiosta 10.0.8 alkaen. Varmista, että "ProductSearch.UseAzureSearch" on määritetty arvoon 'true' kohdassa **Kaupan parametrit > Määrityksen parametrit**. 
![Määrityksen parametrit pilvipohjaiselle haulle.](./media/CloudPoweredSearchConfigurationParameters.png)
>Lajittelun lisävaihtoehdot, kuten uusi, parhaiten myyvä ja suosittu, ovat käytettävissä Commerce SSK -versiossa 9.35+ Dynamics 365 Commercen 10.0.20-versiossa.  


## <a name="additional-resources"></a>Lisäresurssit

[Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md)

[SEO-metatietojen hallinta](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]

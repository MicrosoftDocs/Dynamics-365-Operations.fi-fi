---
title: Hallitse luokituksia ja arvosteluja
description: Tässä ohjeaiheessa käsitellään luokitusten ja arvostelujen hallintaa Microsoft Dynamics 365 Commerce -sivustonmuodostimessa.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8ab85605bce11934f71237ad1ef7cd24804319b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250801"
---
# <a name="manage-ratings-and-reviews"></a>Hallitse luokituksia ja arvosteluja

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään luokitusten ja arvostelujen hallintaa Microsoft Dynamics 365 Commerce -sivustonmuodostimessa.

## <a name="overview"></a>Yleiskuvaus

Dynamics 365 Commerce käyttää Microsoft Azure Cognitive Service -palvelua arvostelun tekstin automaattisessa valvonnassa havaitsemalla sopimattomat sanat. Valvojat voivat toteuttaa myös seuraavat manuaaliset tehtävät Dynamics 365 Commerce -sivustonmuodostimessa.

- Arvostelujen valvominen vastaamalla niihin tai poistamalla ne.
- Asiakkaan arvostelujen poistaminen asiakkaan pyynnöstä.
- Joukkotuonnin luokitusten ja arvostelujen tiedot kaikille tuotteille Microsoft Power BI -mallissa niin, että luokitusten ja arvostelujen trendit voidaan analysoida.

## <a name="read-a-review"></a>Arvostelun lukeminen 

Commerce-sivustonmuodostimessa voi lukea arvostelun seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.
1. Suodata tuotteen arvostelut tuotteen tunnuksen, tuotteen nimen tai arvostelun tekstin mukaan sivun oikeassa yläkulmassa olevan hakukentän avulla.

Lisäsuodattimien avulla voit rajoittaa arvosteluita kauden, arvioinnin, kanavan tai vaikutuksen tila (poistettu, vastattu tai raportoitu).

![Valvonnan aloitussivu](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Arvosteluun vastaaminen 

Joskus tuotteen ostaneet asiakkaat ilmaisevat tyytyväisyyttä tai tyytymättömyyttä tai he eivät tiedä, miten tuotetta käytetään. Valvoja voi vastata arvosteluun. Tämä vastaus näkyy yhdessä arvostelun kanssa sivustossa. 

Commerce-sivustonmuodostimessa voi vastata arvostelun seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.
1. Etsi ja valitse arvostelu, johon haluat vastata.
1. Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää vastaus**.
1. Kirjoita vastauksen teksti ja nimi, jonka haluat näkyvän vastaajan kohdalla. Vastaajan oletusnimi on **valvoja**.
1. Kun olet valmis, valitse **Kirjaa vastaus**.

![Arvosteluun vastaaminen](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Arvostelun poistaminen 

Joskus valvojien kannattaa poistaa asiakkaiden arvosteluita liiketoiminnallisista syistä. 

Commerce-sivustonmuodostimessa voi poistaa arvostelun seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.
1. Etsi ja valitse arvostelu, jonka haluat poistaa.
1. Valitse oikeassa ominaisuusruudussa poiston syy **Poista arvostelu** -kohdassa ja valitse sitten **Poista**.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Asiakkaan arvostelujen poistaminen asiakkaan pyynnöstä 

Joskus asiakkaat haluavat, että luokitukset ja arvostelut poistetaan pysyvästi sähköisen kaupankäynnin sivustosta. Valvoja, joka vastaanottaa poistopyynnön asiakkaalta, voi poistaa asiakkaan tiedot käyttämällä arvostelun poistotoimintoa. Valvoja tarvitsee asiakkaan sen sähköpostiosoitteen, jota on käytetty sisäänkirjauksessa ja arvostelujen antamisessa, jotta hän voi etsiä ja poistaa asiakkaan tiedot. 

Commerce-sivustonmuodostimessa voi etsiä asiakkaan tietoja ja poistaa niitä seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Poista**.
1. Anna **Hae käyttäjiä sähköpostiosoitteen avulla** -ruutuun asiakkaan sähköpostiosoite ja valitse sitten **Hae**.
1. Jos asiakkaalla on arvosteluaktiviteetteja (esimerkiksi arvostelun lähetyksiä, äänestyksiä toisen asiakkaan arvosteluista tai kommentteja toisen asiakkaan arvostelusta), näkyvissä on tuloksia. Jokaisen nimikkeen kohdalla on **Poista**-painike.
1. Valitse jokaisen poistettavan nimikkeen kohdalla **Poista**. Kun sinulta kysytään vahvistusta, valitse **Kyllä**. 
    
![Asiakkaan tietojen poistaminen](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Tietojen poistaminen kokonaan järjestelmästä voi kestää jopa seitsemän päivää. Valvojien tulee ilmoittaa asiakkaille tästä viivästyksestä.
> - Jos asiakkaat ovat muuttaneet nimensä tilin asetuksissa, hakutuloksissa saattaa näkyä useita nimikkeitä. Tässä tapauksessa asiakkaan tietojen poistaminen kokonaan edellyttää, että valvoja valitsee **Poista**-kohdan kaikille nimikkeille. 

## <a name="download-ratings-and-reviews-data"></a>Luokitusten ja arvostelujen tietojen lataaminen

Commerce-sivustonmuodostimessa avulla valvojat voivat tuoda luokitusten ja arvostelujen tiedot joukkona ja analysoida trendejä. Perusmittarit sisältävä Power BI -malli on käytettävissä. Tämän mallin avulla valvojat voivat yhdistää joukkona tuodut tiedot ja tarkastella koontinäyttöä. Heidän ei tarvitse luoda mukautettua koontinäyttöä. Valvojat voivat myös mukauttaa Power BI -mallin vastaamaan erityistarpeita. 

Commerce-sivustonmuodostimessa voi ladata luokituksia ja arvosteluja seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Raportointi**.
1. Valitse **Lataa arvostelun tiedot**, jos haluat ladata luokitusten ja arvostelujen tiedot joukkona CSV-muodossa.

## <a name="view-ratings-and-reviews-trends"></a>Luokitusten ja arvostelujen trendien tarkasteleminen

Valvojat voivat ladata Power BI -mallin niin, että he voivat tarkastella trendejä koontinäytössä.

Commerce-sivustonmuodostimessa voi tarkastella luokitus- ja arvostelutrendejä seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Raportointi**.
1. Lataa malli valitsemalla **PowerBI-malli**.

    ![Power BI -mallin lataaminen](media/rnr-moderation-reports.png) 

1. Avaa ladattu malli käyttämällä Power BI -sovellusta. Sulje näyttöön avautuva **Verkkosisällön käyttöoikeus** -valintaikkuna ja sulje sitten näyttöön tuleva Päivitys-virhesanoma.
1. Siirry kohtaan **Aloitus**, valitse **Muokkaa kyselyitä** ja valitse sitten **Tietolähteen asetukset**.
1. Valitse **Tietolähteen asetukset** -valintaikkunassa **Muuta lähdettä**.
1. Syötä **URL-osoite**-kenttään edellisessä proseduurissa ladattujen arvostelujen tietojen polku (esimerkiksi **c:\\reviews\\ReviewsData.csv**).

    ![URL-osoite-kenttä CSV-valintaikkunassa](media/rnr-powerbi-datasource-settings.png) 

1. Valitse **OK** ja valitse sitten **Käytä muutoksia**. Muutokset otetaan käyttöön tietolähteessä muutaman minuutin kuluessa.
1. Valitse **Trendien taulukko**, jos haluat tarkastella luokitusten ja arvostelujen trendejä.

    ![Luokitusten ja arvostelujen trendit](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Osallistu käyttääksesi luokituksia ja arvosteluja](opt-in-ratings-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)

[Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Verkkokanavaraporttien luominen
description: Tässä artikkelissa kuvataan, miten Microsoft Dynamics 365 Commercessa luodaan raportteja verkkokanavassa.
author: josaw1
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 0523e74d2bfb4191e467edc001daf9178c7b4bf6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268316"
---
# <a name="generate-online-channel-reports"></a>Verkkokanavaraporttien luominen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, miten Microsoft Dynamics 365 Commercessa luodaan raportteja verkkokanavassa.

Voit luoda ja tarkastella useita Commerce-raportteja. Ne osoittavat, miten verkkokanava toimii.

## <a name="channel-summary-report"></a>Kanavan yhteenvetoraportti

**Kanavan yhteenveto** -raportissa näkyy yhteenveto valitun kanavan seuraavista tapahtumista:

- Myyntitapahtumat
- Maksutapahtumat
- Verotapahtumat
- Alennustapahtumat

Voit luoda **Kanavan yhteenveto** -raportin seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan yhteenveto -raportti**.
1. Syötä päivämäärä **Päivämäärästä**-kenttään.
1. Kirjoita päivämäärä **Päivämäärään**-kenttään.
1. Valitse **Kanava**-kentässä verkkokanava.
1. Valitse **OK**.
 
## <a name="channel-sales-by-year-report"></a>Vuosikohtaisen kanavamyynnin raportti 

**Kanavan myynti vuoden mukaan** -raportissa näkyy tietyn myymälän vuosittaisen myynnin vertailu. Valitse vuosi, jonka myyntiä verrataan. Raportti vertaa valitun vuoden myyntiä edellisen vuoden myyntiin.

Voit luoda **Kanavan myynti vuoden mukaan** -raportin seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan vuosikohtainen myynti -raportti**.
1. Anna vuosi **Kalenterivuodesta**-kenttään.
1. Anna vuosi **Kalenterivuoteen**-kenttään.
1. Valitse **Kanava**-kentässä verkkokanava.
1. Valitse **OK**.

## <a name="channel-sales-by-hour-report"></a>Tuntikohtaisen kanavamyynnin raportti

**Kanavan myynti tunnin mukaan** -raportti näyttää valitun kanavan tai toimintoyksikön myyntimittarin tunnin mukaan.

Voit luoda **Kanavan myynti tunnin mukaan** -raportin seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan tuntikohtainen myynti -raportti**.
1. Syötä päivämäärä **Päivämäärästä**-kenttään.
1. Kirjoita päivämäärä **Päivämäärään**-kenttään.
1. Valitse **Kanava**-kentässä verkkokanava.
1. Valitse **OK**.

## <a name="top-customers-report"></a>Suurimpien asiakkaiden raportti

**Parhaat asiakkaat** -raportissa on myyntimittarit parhaille *N* asiakkaille valitussa kanavassa tai toimintoyksikössä. Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.

Voit luoda **Parhaat asiakkaat** -raportin seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat asiakkaat -raportti**.
1. Syötä päivämäärä **Päivämäärästä**-kenttään.
1. Kirjoita päivämäärä **Päivämäärään**-kenttään.
1. Valitse **Kanava**-kentässä verkkokanava.
1. Valitse **OK**.

## <a name="top-discounts-report"></a>Parhaat alennukset -raportti

**Parhaat alennukset** -raportissa on myyntimittarit parhaille *N* alennuksille valitussa kanavassa tai toimintoyksikössä. Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.

Voit luoda **Parhaat alennukset** -raportin seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat alennukset -raportti**.
1. Syötä päivämäärä **Päivämäärästä**-kenttään.
1. Kirjoita päivämäärä **Päivämäärään**-kenttään.
1. Valitse **Kanava**-kentässä verkkokanava.
1. Valitse **OK**.

## <a name="top-products-report"></a>Parhaat tuotteet -raportti

**Parhaat tuotteet** -raportissa on myyntimittarit parhaille *N* tuotteille valitussa kanavassa tai toimintoyksikössä. Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.

Voit luoda **Parhaat tuotteet** -raportin seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat tuotteet -raportti**.
1. Syötä päivämäärä **Päivämäärästä**-kenttään.
1. Kirjoita päivämäärä **Päivämäärään**-kenttään.
1. Valitse **Kanava**-kentässä verkkokanava.
1. Valitse **OK**.

## <a name="category-sales-report"></a>Luokan myyntiraportti

**Luokan myynti** -raportissa näkyvät myyntimittarit valittuna kautena jokaiselle luokkahierarkian solmulle valitussa kanavassa tai toimintoyksikössä.

Voit luoda **Luokan myynti** -raportin seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Luokan myyntiraportti**.
1. Syötä päivämäärä **Päivämäärästä**-kenttään.
1. Kirjoita päivämäärä **Päivämäärään**-kenttään.
1. Valitse **Kanava**-kentässä verkkokanava.
1. Valitse **OK**.

## <a name="organization-sales-report"></a>Organisaation myyntiraportti

**Organisaation myynti** -raportti näyttää myymälöiden suorituskyvyn organisaatioyksiköiden mukaan. Tämä raportti sisältää myynnin määrän ja summan myymälän mukaan sekä kunkin myymälän katetuoton. Organisaatioyksikkö perustuu oletusraportointihierarkiaan.

Voit luoda **Organisaation myynti** -raportin seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Organisaation myyntiraportti**.
1. Syötä päivämäärä **Päivämäärästä**-kenttään.
1. Kirjoita päivämäärä **Päivämäärään**-kenttään.
1. Valitse **OK**.

## <a name="additional-resources"></a>Lisäresurssit

- [Kaupan aloitussivu](./index.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

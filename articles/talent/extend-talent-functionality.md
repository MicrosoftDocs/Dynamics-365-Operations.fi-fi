---
title: Microsoft Dynamics 365 for Talent -sovelluksen toimintojen laajentaminen
description: "Jos olet luonut jonkin Microsoft PowerApps -sovelluksen, voit käynnistää sovelluksen Microsoft Dynamics 365 for Talent -sovelluksen linkin avulla."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cfd3b475b113fdab4ceeb3e636fea6c9134ab982
ms.openlocfilehash: 0ab829803634871c9060daa381bd02d7d2bbdf42
ms.contentlocale: fi-fi
ms.lasthandoff: 12/01/2017

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent -sovelluksen toimintojen laajentaminen

[!include[banner](includes/banner.md)]

Jos olet luonut jonkin Microsoft PowerApps -sovelluksen, voit käynnistää sovelluksen Microsoft Dynamics 365 for Talent -sovelluksen linkin avulla. Voit määrittää sovellusten käyttöoikeuden, kun olet määrittänyt tietyt tiedot Talent-sovelluksen määrityssivulla. Voit avata sivun **Järjestelmän hallinta** -työtilassa.

## <a name="configuring-embedded-powerapps-within-talent"></a>Upotetun PowerApps-sovelluksen määrittäminen Talent-sovelluksessa
Määritä Talent-sivut **Upotetun Microsoft PowerApps -sovelluksen määrittäminen** -sivulla ja aloita PowerApps-sovellusten käyttäminen. Kun haluat avata **Upotetun Microsoft PowerApps -sovelluksen määrittäminen** -sivun, avaa **Järjestelmän hallinta** -työtila ja avaa sitten **Linkit**-välilehti. Valitse **Asetukset**-ryhmässä **Microsoft PowerApps**. 

Sivulla annetaan tai määritetään seuraavat tiedot: 

> - Kunkin PowerApps-sovelluksen kuvaava nimi tai tunnus.
> - Kunkin Talent-sivulle lisättävän sovellusten yksilövä tunnus (GUID). Sovelluksen tunnus on PowerApps-sivustossa osoitteessa [powerapps.com](http://powerapps.com/). 
> - Sivu, jonka avulla käyttävät voivat avata sovelluksen tai raportin. Kaikki Talent-sivut eivät tue upotettuja PowerApps-sovelluksia ja Power BI -raportteja. 

 > [!NOTE]
 >  Anna sivun sisäinen nimi sivun yläosassa olevan näyttönimen sijaan. Löydät sisäisen nimen avaamalla sivun, jonka sisäistä nimeä etsit, ja napsauttamalla hiiren kakkospainikkeella mitä tahansa sivun kohtaa. Kun valikko avautuu, valitse **Lomaketiedot**-kohta osoittamalla sitä. Sisäisen lomakkeen nimi näkyy valikon **Lomaketiedot**-kohdan vieressä.
 
> - Määritä lomakkeen ohjausobjekti, josta sovellus voi hakee kontekstitiedot. Sovelluksessa voidaan käyttää esimerkiksi työntekijää koskevia tietoja. Jos syötät **Konteksti**-kenttään **Työntekijä**-sivun, sovelluksen käynnistyessä avautuu **Työntekijä**-sivu. **Konteksti-kenttään** ei ole pakko syöttää tietoja. 
> - Määritä sen valintaikkunan koko, jossa PowerApps-sovellus suoritetaan. Valintaikkunoiden koko on määritetty pieneksi tai suureksi sovelluksen puhelimen tai suuremman laitteen käyttöliittymässä suorittamisen optimoimista varten. 

Voit määrittää myös oikeushenkilöt, joiden käytettävissä sovellus on, tai määrittää sovelluksen kaikkien oikeushenkilöiden käyttöön. Oletusarvoisesti PowerApps-sovellukset ovat kaikkien oikeushenkilöiden käytettävissä.

## <a name="opening-an-application"></a>Sovelluksen avaaminen
Kun upotetut PowerApps-sovellukset on määritetty, Talent-sovelluksen sivuille lisätään määrittämiesi sovellusten linkit. Valitse linkki, kun haluat avata sovelluksen. 




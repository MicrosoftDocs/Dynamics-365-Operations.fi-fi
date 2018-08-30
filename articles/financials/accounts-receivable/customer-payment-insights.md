---
title: Asiakkaan maksutavat (esikatselu)
description: "Tässä aiheessa kuvataan, miten voit asiakkaan maksutapojen avulla arvioida, milloin lasku maksetaan ja auttaa organisaatioita luomaan optimointistrategioita, jotka parantavat maksujen ajallaan maksamisen todennäköisyyttä."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="customer-payment-insights-preview"></a>Asiakkaan maksutavat (esikatselu)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Tämä ominaisuus on kohdistetun version osa ja on saatavilla vain käyttäjille, jotka ovat valinneet yksityisen esikatselun. Tämä ominaisuus sisältyy tulevaan yleisesti saatavilla olevaan versioon.

# <a name="overview"></a>Yleiskuvaus

Organisaatiot pitävät usein haastavana ennustaa milloin asiakas maksaa laskut. Näiden tietojen puute voi aiheuttaa virheellisiä kassavirtaennusteita, tehottomia perintäprosesseja ja tilausten toimittamista asiakkaille, jotka voivat luoda luottoriskin. Asiakkaan maksutavat (esikatselu) käyttää automaattianalyysiä ennustaakseen milloin lasku maksetaan. Se tarjoaa myös optimointistrategioita, joita voidaan räätälöidä niin, että voidaan maksimoida todennäköisyys sille, että asiakkaat maksavat ajoissa.

## <a name="predictions"></a>Ennusteet

Maksuennusteiden avulla organisaatiot voivat parantaa yritysprosessejaan seuraavin tavoin:

-   Tunnistaa helposti laskut, jotka todennäköisesti maksetaan myöhässä.
-   Tehdä tarvittavat toimenpiteet parantaakseen todennäköisyyttä, että maksu maksetaan ajoissa.

Asiakkaan maksutavat (esikatselu) käyttää automaattianalyysiä ennustaakseen milloin lasku maksetaan. Käyttää historiatietoja laskuista, maksuista ja asiakastiedoista luodakseen automaattianalyysin, jonka avulla voi ennustaa milloin lasku maksetaan.

Asiakkaan maksutavat (esikatselu) ennustaa kolme maksun todennäköisyyttä kullekin avoimelle laskulle:

-  Todennäköisyys sille, että maksu suoritetaan ajoissa (laskun eräpäivään mennessä).
-  Todennäköisyys sille, että maksu suoritetaan 30 päivän kuluessa laskun eräpäivästä.
-  Todennäköisyys sille, että maksu suoritetaan 30 päivän jälkeen laskun eräpäivästä.

Maksujen todennäköisyyksiä voidaan tarkastella ennusteosiossa.

[![Maksuennusteet](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Jokaisella laskulla on myös määritetty voittava maksujen todennäköisyys käyttäen jotakin yllä kuvatuista kolmesta ennalta määritellystä maksun todennäköisyysskenaariosta. Skenaario, jolla on suurin maksun todennäköisyys on voittanut skenaario.


Oletetaan esimerkiksi, että laskun ennuste näyttää 71 prosenttia sille, että lasku maksetaan ajoissa, 13 prosenttia sille, että lasku maksettu 30 päivän sisällä eräpäivästä ja 16 prosentin todennäköisyyttä sille, että lasku maksetaan yli 30 päivää eräpäivän jälkeen. Suurin todennäköisyys ilmaisee, että lasku on ajoissa-skenaariossa siten, että lasku merkitään todennäköisesti ajallaan maksettavaksi.

[![Maksuennusteet](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Optimointistrategiat

Maksuennusteiden lisäksi asiakkaan maksutapojen (esikatselu) avulla voit käyttää optimointistrategioita parantaaksesi mahdollisuuksia saada maksu ajoissa. Tämä antaa organisaatioille mahdollisuuden tehdä ”mitä jos” -analyysejä antamalla käyttäjien oikaista laskuja ja asiakasparametrejä ja sitten verrata vaikuttaako tämä todennäköisyyteen saada maksut ajoissa.

Organisaatio voi esimerkiksi halutessaan arvioida vaikuttaako käteisalennuksen päivittäminen laskuihin maksujen ajallaan saamisen todennäköisyyttä. Kun laskut on optimoitu käyttämään uutta alennusta, käyttäjät voivat tarkistaa parantaako alennuksen lisääminen todennäköisyyttä saada maksu ajoissa. Mikäli alennuksen lisääminen kustantaa vain vähän verrattuna sen tuomaan etuun ajallaan saadusta maksusta, organisaatio voi valita kohdistavansa alennuksen kaikkiin tuleviin avoimiin tilauksiin.

> [!NOTE] 
> Tällä hetkellä vain alennus on käytettävissä optimointistrategiana asiakkaan maksutavassa (esikatselu).

[![Optimoidut ennusteet](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Miten saada asiakkaan maksutavat (esikatselu)

Mikäli haluat kokeilla asiakkaanmaksutapoja (esikatselu), lähetä sähköpostia [Finance Insights Preview team](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Tietosuojatiedot

Esikatselut tallentavat asiakkaan tiedot Yhdysvalloissa. Lisäksi esikatselu (1) voi käyttää vähemmän tietosuojaa ja suojaustoimenpiteet kuin Dynamics 365 for Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) ei pidä käyttää henkilötietojen tai muiden sellaisten tietojen prosessoimiseen, joita koskevat lait tai määräykset, ja (4) sillä on rajoitettu tuki.


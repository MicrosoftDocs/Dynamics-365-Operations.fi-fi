---
title: Kirjaaminen johdettujen kirjojen kanssa
description: "Tässä artikkelissa kerrotaan, miten johdettuja kirjoja käytetään."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: ca077727910059878fb16a3f78c5b9133c6c741f
ms.lasthandoff: 03/31/2017


---

# <a name="post-with-derived-books"></a>Kirjaaminen johdettujen kirjojen kanssa

Tässä artikkelissa kerrotaan, miten johdettuja kirjoja käytetään.

Kun tapahtuma kirjataan kirjaan, joka sisältää johdettuja kirjoja, johdettua kirjaa koskevat tapahtumat kirjautuvat automaattisesti kirjauskansioihin, ostotilauksiin tai vapaatekstilaskuihin. Jos kuitenkin valmistelet ensisijaisen kirjan tapahtumat Käyttöomaisuus-kansioon, voit tarkastella ja muuttaa johdettujen tapahtumien määriä ennen niiden kirjaamista.
-   Tietyt tilit, kuten arvonlisävero-, asiakas- tai toimittajatilit, päivittyvät vain kerran ensisijaisen kirjan kirjauksilla. Johdetun kirjan tapahtumat kirjautuvat tileille, jotka on määritetty johdetulle kirjalle Käyttöomaisuuserän kirjausprofiilit -sivulla.
-   Hankinta on usein käytetty johdetun kirjan tapahtumalaji. Sitä voidaan käyttää, kun kirja ja johdettu kirja olisi liitettävä käyttöomaisuuserään omaisuuserän hankintahetkestä alkaen.
-   Myös muita tapahtumatyypin arvoja voi olla käytössä. Jos esimerkiksi ensisijaisella kirjalla ja johdetuilla kirjalla on samat myyntiä tai luovutusta koskevat aikavälit, kaikki käyttöomaisuuden tapahtumatyypit ovat käytettävissä johdettua poistokirjaa määritettäessä.

> [!WARNING]
> Johdetussa kirjassa kirjattu poisto on saman suuruinen kuin ensisijaiselle kirjalle kirjattu poisto. Jos kahden kirjan poistomenetelmät eivät ole samanlaiset, poistotapahtumia ei pitäisi luoda johdettua prosessia käyttämällä. |

## <a name="example"></a>Esimerkki 
Seuraavaksi kuvataan, miten hankintatapahtumat määritetään johdetun kirjan toiminnoilla.

1.  Luo kirjat Kirjat-sivulle.
    -   Kirja kirjanpitoa varten: AM 1, Nykyinen kirjanpitotaso
    -   Kirja verotusta varten: AM 2, Verotuksen kirjanpitotaso

2.  Valitse AM 1:ssä Johdetut kirjat -välilehti. Valitse Kirja-kentästä AM 2 ja Tapahtumatyyppi-kentästä Hankinta.

Kirjat voidaan sitten liittää tiettyihin käyttöomaisuuseriin. 

Kun hankintahinta kirjataan käyttöomaisuuserälle on kirja-VM 1, hankinta kirjataan vain AM 1: een, vaan myös johdettu kirjan AM 2. Käyttöomaisuuserän molempien kirjojen tilaksi Avoin.

> [!NOTE]                                                                                                         
> Jos et käytä johdettuja poistokirjoja, sinun on tehtävä käyttöomaisuuden hankintahinnan kirjaus sekä kirjaa AM 1 että kirjaa AM 2 varten.

Lisätietoja on ohjeaiheessa [johdetut poistokirjat](derived-books.md)



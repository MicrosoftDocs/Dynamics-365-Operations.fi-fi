---
title: Kirjaaminen johdettujen kirjojen avulla
description: Tässä artikkelissa kerrotaan, miten johdettuja kirjoja käytetään.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6556965a1356522de5f4c17ddeab378a128fbe3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833015"
---
# <a name="post-with-derived-books"></a>Kirjaaminen johdettujen kirjojen avulla

[!include [banner](../includes/banner.md)]

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

2.  Valitse AM 1:ssä Johdetut kirjat -välilehti ja valitse Kirja-kentästä AM 2 ja Tapahtumatyyppi-kentästä Hankinta.

Kirjat voidaan sitten liittää tiettyihin käyttöomaisuuseriin. 

Kun hankintahinta kirjataan käyttöomaisuudelle, jonka kirja on AM 1, hankintahinta ei kirjaudu vain AM 1:een, vaan myös johdettuun kirjaan AM 2. Kummankin käyttöomaisuuskirjan tilaksi päivitetään yleensä Avoin.

> [!NOTE]                                                                                                         
> Jos et käytä johdettuja poistokirjoja, sinun on tehtävä käyttöomaisuuden hankintahinnan kirjaus sekä kirjaa AM 1 että kirjaa AM 2 varten.

Lisätietoja on kohdassa [Johdetut kirjat](derived-books.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
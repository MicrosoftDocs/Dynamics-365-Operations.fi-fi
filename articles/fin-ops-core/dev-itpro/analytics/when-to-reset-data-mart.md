---
title: Tietovaraston osajoukon usein kysytyt kysymykset
description: Tämä ohjeaihe sisältää vastauksia eräisiin usein kysyttyihin tietovaraston osajoukon kysymyksiin.
author: jinniew
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 53f45f469c39f9e389763aa0daed658e5a62d377
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119509"
---
# <a name="data-mart-resets-faq"></a>Tietovaraston osajoukon usein kysytyt kysymykset

Tämä ohjeaihe sisältää vastauksia eräisiin usein kysyttyihin tietovaraston osajoukon kysymyksiin. Tietojen nollaaminen voi olla aika vievä prosessi, eikä se olosuhteista riippuen välttämättä ole tarvittava ratkaisu. Siksi tämä ohjeaihe sisältää tietoja olosuhteista, joissa tietojen nollaaminen voi auttaa, sekä olosuhteista, joissa se ei todennäköisesti auta.

## <a name="what-is-a-data-mart-reset"></a>Mikä on tietovaraston osajoukon palauttaminen?

Tietojen nollaaminen poistaa integrointitehtävät käytöstä, poistaa kaikki tiedot ja ottaa integroinnin uudelleen käyttöön.

Jotta voidaan varmistaa, että vanhoja tietoja ei lisätä, tietojen uudelleen nollaaminen voidaan aloittaa vasta, kun aiemmin luodut tehtävät on suoritettu. Jos yrität nollata tiedot ennen kaikkien tehtävien suorittamista, näyttöön voi tulla seuraava sanoma: "Tietojen uudelleen nollaaminen ei onnistunut aktiivisen tehtävän vuoksi. Yritä myöhemmin uudelleen."

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Milloin tietovarasto on nollattava?

Jos jokin seuraavista lausekkeista on voimassa tilanteessasi, organisaatiosi voi käyttää tietojen nollaamista:

- **Sovellustietokanta palautettiin**
- **Tukipalvelupyyntö on avattu** – Tukihenkilö on ohjeistanut nollaamaan tietovaraston vianmääritysvaiheen osana.
- **Suuri vanhentuneiden tietueiden prosenttiosuus** – Tietueiden vanhentuminen ei välttämättä edellytä tietovaraston nollaamista. Suuret vanhentuneiden tietueiden prosenttiosuudet voivat heikentää yleistä raporttien luonnin ja integroinnin suorituskykyä ja aiheuttaa suurempaa tietokantatilan käyttöä. On suositeltavaa suorittaa datamart-nollaus vanhentuneiden tietojen poistamiseksi, kun datamartin vanhentuneiden tietojen osuus on yli 80 %.
 
> [!NOTE]
> Tietojen tarjoajan nollausprosessiin vaikuttaa tietokannassa olevien pääkirjanpito- ja budjettitapahtumien määrä. Järjestelmäsi tapahtumien määrän mukaan tietojen tarjoajan nollaus voi kestää jopa ainoastaan 15 minuuttia tai enintään neljä tuntia. Jos nollaus kestää yli neljä tuntia, suosittelemme, että otat yhteyttä tukeen.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Milloin tietovaraston osajoukon palautus ei kannata?

Tässä on joitain tilanteita, joissa emme suosittele tietovaraston nollaamista:

- Sinulla on ongelmia tietojen integroinnin suorituskyvyn kanssa.
- Nollausmalli toistuu jonkin seuraavan syyn vuoksi:

    - **Raportista puuttuu tietoja tai siinä on odottamattomia tietoja** – Jos havaitset, että tietoja puuttuu, avaa Microsoftille tukipalvelupyyntö, jonka avulla voit tarkistaa raporttisi muodon ja mahdolliset tietojen synkronointiongelmat.
    - **Juuttunut integroinnin tila**
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Jos tietovaraston osajoukko palautetaan, menetetäänkö jo suunnitellut raportit?

Et voi. Raportit tallennetaan SQL-tauluihin, joihin tietovaraston osajoukon nollaaminen ei vaikuta. Jos olet huolissasi suunnittelemiesi raporttien menettämisestä, voit varmuuskopioida mallit, joita et halua menettää. Voit varmuuskopioida suunnitelmasi avaamalla Report Designerin ja valitsemalla **Yritys \> Yritykset \> Rakenneosat \> Vie**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Onko kaikkien käyttäjien poistuttava järjestelmästä, ennen kuin voin nollata tiedot?

Et voi. Käyttäjät voivat jatkaa järjestelmässä työskentelyä tietovaraston osajoukon nollaamisen aikana. Käyttäjät eivät kuitenkaan voi käyttää Financial Reporterilla luotuja raportteja, ennen kuin nollaus on valmis.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Asiakasportaalin käyttäjien luominen ja hallinta (sisältää videon)
description: Tässä ohjeaiheessa selitetään, miten voit luoda asiakasportaalin käyttäjätilejä ja määrittää niiden käyttöoikeuksia.
author: Henrikan
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4615182e6c3341a376e8e55a1417480e3e3f5ea7
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062487"
---
# <a name="create-and-manage-customer-portal-users"></a>Asiakasportaalin käyttäjien luominen ja hallinta

[!include [banner](../includes/banner.md)]


Käyttöönottototeutuksessa käyttäjät eivät voi rekisteröityä itse verkkosivustoihin, jotka luodaan asiakasportaalin avulla. Kirjautuminen ja sivuston käyttäminen edellyttää, että järjestelmänvalvoja kutsuu käyttäjät. Microsoft on tarkoituksellisesti torjunut käyttäjien mahdollisuuden rekisteröityä itse.

Ennen kuin käyttäjä voi käyttää verkkosivustoa, kyseiselle käyttäjälle on luotava yhteyshenkilötietue. Tämä tietue ilmaisee, mihin asiakastiliin ja yritykseen käyttäjä kuuluu. Nämä tiedot ovat välttämättömiä, jotta voidaan varmistaa, että käyttäjä voi luoda ja tarkastella myyntitilauksia.

Kun käyttäjät rekisteröivät itsensä, niiden yhteystiedot luodaan automaattisesti. Tämän vuoksi et voi varmistaa, että käyttäjä valitsee oikean asiakastilin ja yrityksen. Toisaalta kutsuprosessin avulla järjestelmänvalvoja voi määrittää yhteyshenkilölle oikean asiakastilin ja yrityksen, ennen kuin kutsu lähetetään. Jos olet aikeissa mukauttaa ratkaisua niin, että käyttäjät voivat itse rekisteröityä, muista huomioida mahdolliset seuraukset.

## <a name="video"></a>Video
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

[Asiakkaiden kutsuminen rekisteröitymään ja käyttämään asiakasportaalia](https://youtu.be/drGUYHX9QIQ) -video (alla) sisältyy [Taloushallinnon ja toimintojen toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on YouTubessa.

## <a name="prerequisite-setup"></a>Vaadittavat asetukset

Power Apps -portaalien yhteyshenkilöt tallennetaan **yhteyshenkilöt** -taulukon tietueiksi Microsoft Dataverseen. Kaksoiskirjoitus synkronoi sitten nämä tiedot Microsoft Dynamics 365 Supply Chain Managementille tarpeen mukaan.

![Asiakasportaalin yhteyshenkilöiden järjestelmäkaavio.](media/customer-portal-contacts.png "Asiakasportaalin yhteyshenkilöiden järjestelmäkaavio")

Ennen kuin aloitat uusien asiakkaiden kutsumisesta, varmista, että **Yhteyshenkilö**-taulukon yhdistämismääritys on otettu käyttöön kaksoiskirjoituksessa.

## <a name="the-invitation-process"></a>Kutsuprosessi

Jos haluat kutsua aiemmin luodun yhteyshenkilön asiakasportaaliin, noudata ohjeita kohdassa [yhteystietojen kutsuminen portaaleihin](/powerapps/maker/portals/configure/invite-contacts) Power Apps -portaalien dokumentaatiossa.

Ennen kuin kutsut asiakkaan liittymään asiakasportaaliin, varmista, että asiakkaan [yhteyshenkilötietue](/powerapps/maker/portals/configure/configure-contacts) on käytettävissä ja määritetty seuraavalla tavalla:

1. Aseta **Yritys**-kenttä yritykselle, johon haluat asiakkaan kuuluvan Supply Chain Managementissa.
2. Aseta **Tilinumero**-kenttä siihen asiakastilinumeroon, jonka haluat asiakkaalla olevan Supply Chain Managementissa.

Kun yhteyshenkilö on perustettu, sen voi nähdä Supply Chain Managementissa.

Lisätietoja on ohjeaiheessa [yhteystiedon määrittäminen käytettäväksi](/powerapps/maker/portals/configure/configure-contacts) Power Apps -portaalien dokumentaatiossa.

## <a name="out-of-box-web-roles-and-table-permissions"></a>Valmiit verkkoroolit ja taulukon käyttöoikeudet

Power Apps -portaalien käyttäjäroolit määritetään [verkkoroolien](/powerapps/maker/portals/configure/create-web-roles) ja [taulukon käyttöoikeuksien](/powerapps/maker/portals/configure/assign-entity-permissions) mukaan. Asiakasportaalille määritetään joitakin valmiita rooleja. Voit luoda uusia rooleja ja muokata tai poistaa aiemmin luotuja rooleja.

### <a name="out-of-box-web-roles"></a>Valmiit verkkoroolit

Tässä osassa kuvataan asiakasportaalin mukana toimitetut verkkoroolit.

Lisätietoja muiden käyttäjien roolien muokkaamisesta on kohdissa [Verkkoroolien luominen portaaleihin](/powerapps/maker/portals/configure/create-web-roles) ja [Tietuepohjaisen suojauksen lisääminen portaalien taulukko-oikeuksien avulla](/powerapps/maker/portals/configure/assign-entity-permissions) Power Apps -portaalien dokumentaatiossa.

#### <a name="administrator"></a>Järjestelmänvalvoja

Ylläpitäjä valvoo ja ylläpitää verkkosivustoa. Tämä henkilö laatii ja määrittää asiakasportaalin. Järjestelmänvalvoja ylläpitää portaalin tietoturva- ja suojausnäkökohtia ja varmistaa, että kaikki sujuu ongelmitta. Järjestelmänvalvoja voi myös mukauttaa ja/tai muuttaa portaalia lisäämällä uusia toimintoja, luomalla uusia rooleja ja paljon muuta.

#### <a name="customer-representative"></a>Asiakkaan edustaja

Asiakkaan edustaja työskentelee asiakasyrityksessä ja vastaa yrityksen käyttämien tilausten hallinnasta. Asiakkaan edustaja näkee kaikki tilaukset, jotka yritykselle ja niille asettaneelle käyttäjälle on asetettu. Lisäksi asiakkaan edustaja voi nähdä tietoja yleistilistä ja siitä, mitkä yhteyshenkilöt voivat tehdä tilauksia kyseisen tilin puolesta.

#### <a name="authorized-users"></a>Valtuutetut käyttäjät

Valtuutetut käyttäjät voivat tehdä tilauksia ja tarkastella asettamiaan tilauksia. He eivät kuitenkaan voi tarkastella niiden tilausten tilaa, jotka muut yrityksen käyttäjät ovat asettaneet.

#### <a name="unauthorized-users"></a>Luvattomat käyttäjät

Luvattomat käyttäjät eivät voi tarkastella tietoja. He näkevät vain julkisia tietoja, kuten ehtoja ja tietoja asiakasportaalia suorittavasta yrityksestä.

#### <a name="example"></a>Esimerkki

Seuraavasta taulukosta ilmenee, mitkä myyntitilaukset kunkin verkkoroolin käyttäjät voivat nähdä järjestelmässä.

| Myyntitilaus | Järjestelmänvalvoja | Asiakkaan&nbsp;X asiakasedustaja | Valtuutettu käyttäjä: Jane | Valtuutettu käyttäjä: Sam | Luvattomat käyttäjät: May |
|---|---|---|---|---|---|
| Asiakas&nbsp;X Tilaaja:&nbsp;Jane | Kyllä | Kyllä | Kyllä | Ei | Ei |
| Asiakas&nbsp;X Tilaaja:&nbsp;Sam | Kyllä | Kyllä | Ei | Kyllä | Ei |
| Asiakas&nbsp;Y Tilaaja:&nbsp;May | Kyllä | Ei | Ei | Ei | Ei |

> [!NOTE]
> Vaikka sekä Sam että Jane ovat yhteyshenkilöitä, jotka työskentelevät asiakas X:ssä, he näkevät vain itse asettamiaan tilauksia eikä mitään muuta. Vaikka Maylla on järjestelmässä tilaus, hän ei näe tilausta asiakasportaalissa, koska hän on luvaton käyttäjä. (Lisäksi hän on asettanut tilauksen jonkin muun kanavan kautta kuin asiakasportaali.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
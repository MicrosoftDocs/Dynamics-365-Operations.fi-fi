---
title: Sisällöntoimitusverkon käyttöönottoasetukset
description: Tässä aiheessa on tietoja sisällöntoimitusverkoston (CDN) käyttöönottovaihtoehdoista, joita voidaan käyttää Microsoft Dynamics 365 Commerce -ympäristöissä. Nämä vaihtoehdot ovat alkuperäiset, Commercen tarjoamat Azure Front Door -esiintymät sekä asiakkaiden omistuksessa olevat Azure Front Door -esiintymät.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 944123f3afe1c869c262da3997a73d8c60bbc366
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692722"
---
# <a name="content-delivery-network-implementation-options"></a>Sisällöntoimitusverkon käyttöönottoasetukset

[!include [banner](includes/banner.md)]

Tässä aiheessa on tietoja sisällöntoimitusverkoston (CDN) käyttöönottovaihtoehdoista, joita voidaan käyttää Microsoft Dynamics 365 Commerce -ympäristöissä. Nämä vaihtoehdot ovat alkuperäiset, Commercen tarjoamat Azure Front Door -esiintymät sekä asiakkaiden omistuksessa olevat Azure Front Door -esiintymät.

Commerce-asiakkailla on useita vaihtoehtoja, kun he harkitsevat, mitä CDN-palvelua käytetään Commerce-ympäristössä. Commerce on julkaistu Azure Front Door -perustuella, joka kattaa isännöinnin perusvaatimukset ja mukautetut perustoimialuevaatimukset. Yrityksille, jotka haluavat enemmän hallintaa ja tarkempia suojaustoimintoja, kuten web-sovelluksen palomuurin (WAF), kannattaa käyttää joko asiakkaan omistamaa, Azure Front Door -esiintymää tai ulkopuolista CDN-palvelua.

Commerce-ympäristöissä voidaan käyttää seuraavia kolmea CDN-käyttöönottovaihtoehtoa:

- Commercen mukana toimitettu Azure Front Door -esiintymä
- Asiakkaan omistuksessa oleva Azure Front Door (parempaan hallintaan ja lisäsuojaukseen)
- Ulkoinen CDN-palvelu

Kaikki kolme CDN-asennusvaihtoehtoa toimittavat vain dynaamista HTML-sisältöä mukautetuista toimialueista. Commerce käsittelee automaattisesti kaikki JavaScript-, tyylisivu (CSS)-, kuva-, video- ja muun staattisen sisällön Microsoftin hallitsemalla CDN-palvelulla. Valittava vaihtoehto määrittää käytettävissä olevat toiminnot, hallintaominaisuudet ja lisäsuojausominaisuudet.

Seuraavassa kuvassa on yhteenveto Commerce-arkkitehtuurista.

![Commerce-arkkitehtuurin yleiskuvaus.](media/Commerce_CDN-Option_ComparisonModels.png)

Lisätietoja Azure Front Door -esintymän määrittämisestä Commerce-sivustolle on kohdassa [CDN-tuen lisääminen](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Käytä Commercen mukana toimitettua Azure Front Door -esiintymää

Seuraavassa taulukossa luetellaan Commercen mukana tulevan Azure Front Door -esiintymän hyvät ja huonot puolet sisältöpäätepisteiden hallinnassa.

| Hyvät puolet | Huonot puolet |
|------|------|
| <ul><li>Instanssi sisältyy Commerce-kustannukseen.</li><li>Koska Commerce-tiimi hallitsee instanssia, ylläpitoa on vähemmän ja määritysvaiheet ovat yhteisiä.</li><li>Azuren ylläpitämä infrastruktuuri on skaalattava, suojattu ja luotettava.</li><li>SSL (Secure Sockets Layer) -varmenne edellyttää kerta-asetuksen, ja se uusitaan automaattisesti.</li><li>Commerce-tiimi valvoo virheiden ja poikkeamien varalta.</li></ul> | <ul><li>WAF:ia ei tueta.</li><li>Ei erityisiä mukautuksia tai asetusten muutoksia.</li><li>Esiintymä riippuu Commerce -tiimin päivityksistä tai muutoksista.</li><li>Apex-toimialueita varten on käytettävä erillistä Azure Front Door -esiintymää, jotta Apex-toimialueet voidaan integroida Azure DNS -järjestelmän kanssa.</li><li>Asiakkaalle ei toimiteta telemetriaa vastauksia sekunnissa (RPS) -tiedoista tai virhetasosta.</li></ul> |

Seuraavassa kuvassa esitetään Commercen toimittaman Azure Front Door -esiintymän arkkitehtuuri.

![Commercen mukana toimitettu Azure Front Door -esiintymä.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Asiakkaan omistaman Azure Front Door -instanssin käyttö

Seuraavassa taulukossa luetellaan asiakkaan omistaman Azure Front Door -esiintymän hyvät ja huonot puolet sisältöpäätepisteiden hallinnassa.

| Hyvät puolet | Huonot puolet |
|------|------|
| <ul><li>Määritys on suojattu ja helppo hallita.</li><li>Azuren ylläpitämä infrastruktuuri on skaalattava, suojattu ja luotettava.</li><li>Esiintymä sallii WAF-integroinnin ja hienojakoisen sääntöjen hallinnan erityiseen sivustosi käyttöön säädetyn suojauksen toteuttamiseksi.</li><li>Instanssi sallii SSL-sertifikaattien (sekä asiakkaan omistamien että Azure Front Doorin hallitsemien) ja toimialueiden linkittämisen hienosäädön.</li><li>Esiintymä tarjoaa apex-toimialueratkaisun, jos se on yhteydessä suoraan Azure DNS -järjestelmään.</li><li>Mukana on telemetria ja hälytykset.</li><li>SSL-varmenne edellyttää kerta-asetuksen, ja se uusitaan automaattisesti.</li></ul> | <ul><li>Instanssia hallitaan itse.</li><li>Tietoja ja oppimista pitää aluksi hankkia.</li></ul> |

Seuraavassa kuvassa on Commercen infrastruktuuri, joka sisältää asiakkaan omistaman Azure Front Door -instanssin.

![Commercen infrastruktuuri, joka sisältää asiakkaan omistaman Azure Front Door -instanssin.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Käytä ulkoista CDN-palvelua

Seuraavassa taulukossa on lueteltu ulkoisen CDN-palvelun käyttämisen hyvät ja huonot puolet sisällön päätepisteiden hallinnassa.

| Hyvät puolet | Huonot puolet |
|------|------|
| <ul><li>Tästä vaihtoehdosta on hyötyä, jos olemassa olevaa toimialuetta jo isännöidään ulkoisessa CDN-palvelussa.</li><li>WAF: Riippuu ulkoisesta palveluntarjoajasta.</li></ul> | <ul><li>Erillinen sopimus ja lisäkustannukset tarvitaan.</li><li>SSL-suojaus voi aiheuttaa lisäkustannuksia.</li><li>Koska palvelu on erillinen Azure-pilvipalvelurakenteesta, on hallittava lisää lisäinfrastruktuuria.</li><li>Palvelu saattaa edellyttää pidempiä aikainvestointeja päätepisteen ja suojauksen määritykseen.</li><li>Palvelua hallitaan itse.</li><li>Palvelua valvotaan itse.</li></ul> |

Seuraavassa kuvassa on Commercen infrastruktuuri, joka sisältää ulkoisen CDN-palvelun.

![Commerce-infrastruktuuri, joka sisältää ulkoisen CDN-palvelun.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Lisäresurssit

[Sisällön toimitusverkoston (CDN) tuen lisääminen](add-cdn-support.md)

---
title: Aktiivinen kuvamoduuli
description: Tässä ohjeaiheessa kerrotaan aktiivisista kuvamoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5375a9fc4b168addadadb457b89f5c3ac2ab2746
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638070"
---
# <a name="active-image-module"></a>Aktiivinen kuvamoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan aktiivisista kuvamoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Aktiivista kuvamoduulia voidaan käyttää tuotetunnisteiden upottamiseksi kuvaan. Tämän jälkeen sähköisen kaupankäynnin sivuston käyttäjät voivat siirtää osoittimensa tunnisteiden ylle esikatsellakseen kuvassa näytettyjä tuotteita. Esikatselut näytetään ponnahdusikkunoissa. Käyttäjät voivat valita esikatselun ponnahdusikkunan siirtyäkseen suoraan vastaavan tuotteen tuotetietosivulle (PDP).

Tunnisteet määritetään käyttämällä kuvan X- ja Y-koordinaatteja. Jokaisen tunnistetun pisteen tulisi sisältää kuvassa näytetyn tuotteen tuotetunnus.

Seuraavassa kuvassa on esimerkki esikatselun ponnahdusikkunasta Adventure Worksin kotisivun hero-kuvassa.

![Esimerkki aktiivisen kuvamoduulin esikatselun ponnahdusikkunasta](./media/Active_image.PNG)

> [!IMPORTANT]
> - Aktiivinen kuvamoduuli on käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.
> - Aktiivinen kuvamoduuli on esillä Adventure Works -teemassa.

## <a name="active-image-module-properties"></a>Aktiivisen kuvamoduulin ominaisuudet

| Ominaisuuden nimi      | Arvot | kuvaus |
|--------------------|--------|-------------|
| Kuva              | Kuvatiedosto | Kuvan avulla voidaan esitellä yhtä tai useampaa tuotetta. Kuva voidaan ladata Commerce-sivuston luontiohjelman mediakirjastoon. Myös olemassa olevaa kuvaa voi käyttää. |
| Leveys              | Pikselien määrä | Tämä ominaisuus määrittää kuvan leveyden. Aktiiviset koordinaatit lasketaan kuvan leveyden perusteella.|
| Aktiiviset koordinaatit | X- ja Y-koordinaatit sekä tuotetunnusnumero | Jokainen aktiivinen kuvataulukko koostuu X- ja Y-koordinaateista sekä tuotteen tunnusnumerosta.|
| Otsikko            | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Otsikolle käytetään oletusarvoisesti **H2**-otsikkotunnistetta, mutta tunnistetta voi kuitenkin muuttaa tarvittaessa helppokäyttötoimintojen vaatimusten noudattamiseksi. |
| Kappale          | Kappaleen teksti | Moduuli tukee kappaleen tekstiä RTF-muodossa. Joitakin RTF-ominaisuuksia tuetaan, kuten hyperlinkit, lihavointi, alleviivaus ja kursiivi. Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista. |
| Linkitä               | Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä** -valitsin | Moduuli tukee yhtä tai useampaa toimintokutsulinkkiä. Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia. ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia. Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen. |
| Alateksti           | Otsikko, teksti ja linkit | Kuvalle voidaan lisätä lisätietoja, kuten kirjoittajan tai suunnittelijan nimi, tai linkkejä henkilökohtaisiin blogeihin.|
| Tekstin teema         | **Vaalea** tai **tumma** | Tämän ominaisuuden avulla käyttäjä voi muuttaa tekstin vaaleaksi tai tummaksi taustakuvan perusteella. Se on käytettävissä teemalaajennuksena Adventure Works -teemassa. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Aktiivisen kuvamoduulin lisääminen uudelle sivulle

Voit lisätä aktiivisen kuvamoodulin uudelle sivulle ja määrittää pakolliset ominaisuudet noudattamalla seuraavia ohjeita.

1. Valitse **Mallit** ja avaa sivustosi aloitussivun markkinointimalli (tai luo uusi markkinointimalli).
1. Valitse oletussivun **pääpaikassa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunasta **Aktiivinen kuva** -moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Valitse **Sivut** ja avaa sivuston aloitussivu (tai luo uusi aloitussivu käyttämällä markkinointimallia).
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunasta **Aktiivinen kuva** -moduuli ja valitse sitten **OK**.
1. Lisää aktiivisen kuvamoduulin ominaisuusruutuun kuva ja määritä alustan leveys vastaamaan kuvan kokoa.
1. Määritä X- ja Y-koordinaatit ja lisää asiaankuuluva tuotetunnusnumero.
1. Lisää ja määritä lisää aktiivisia kuvamoduuleita tarpeen mukaan.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Adventure Works -teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

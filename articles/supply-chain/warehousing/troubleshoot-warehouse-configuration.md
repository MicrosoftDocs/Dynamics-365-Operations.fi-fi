---
title: Varaston määrityksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä Microsoft Dynamics 365 Supply Chain Managementia määritettäessä.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60873cb76ee08dd5a4bd4ed8b38cc4845b500453bf34bd10708b105448b58c9a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735084"
---
# <a name="troubleshoot-warehouse-configuration"></a>Varaston määrityksen vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä Microsoft Dynamics 365 Supply Chain Managementia määritettäessä.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Seuraava virhesanoma avautuu: Rekisterikilpi tai sijainti ei kelpaa.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma avautuu,, kun rekisterikilven tunnus tai sijainti skannataan.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varmista, että mikään muu ei ole varannut rekisterikilven tunnusta. Tämä ongelma esiintyi aiemmin, kun käyttäjän varastonhallinnan mobiilisovelluksessa skannaama arvo oli sekä kelvollinen sijainti että kelvollinen rekisterikilven tunnus. Tämä ongelma kuitenkin korjattiin versiossa 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Seuraava virhesanoma avautuu: Tälle sijainnille on määritettävä rekisterikilpi.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma avautuu, jos siirtotilaus luodaan käyttämällä varastoa, jossa on otettu käyttöön edistyksellinen varastonhallinta, ja kun lähetystä yritetään vahvistaa työn valmistumisen jälkeen.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Lähtövaraston kuljetusvaraston **Oletusvastaanottosijainti** -kenttä on tyhjä. Korjaa ongelma määrittämällä oletusvastaanottosijainti kuljetusvarastossa. Varmista, että tämä sijainti on rekisterikilpiohjattu.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Seuraava virhesanoma avautuu: Et voida luoda työmalliriviä kohteelle Varaston tilanmuutos, koska työtyyppi ei ole kelvollinen. Valitse toinen työtyyppi.

### <a name="issue-description"></a>Ongelman kuvaus

Työmallissa ei voi valita *Varaston tilanmuutos* **Työmallin tiedot** -osan **Työtyyppi**-sarakkeessa.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus. Vain järjestelmäprosessit käyttävät *Varaston tilanmuutos* -työtyyppiä. Sitä ei voi määrittää. Koska työtyyppiluettelo on korjattu luettelointina, lisäkohteita ei voi suodattaa pois avattavasta **Työtyyppi**-valikosta.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Seuraava virhesanoma avautuu: Yksikön 1% määrä ei kelpaa.

### <a name="issue-description"></a>Ongelman kuvaus

*Kpl*-yksikön määrä ei kelpaa, jos keräilytyössä on useita rekisterikilpiä yhdessä sijainnissa.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varmista, että vapautetun tuotteen tai tuotevariantin **Yksikön sarjaryhmän tunnus**- ja **Yksikkömuunnokset**-kentät on määritetty oikein.

Huomaa, että virhesanomaa on parannettu versiossa 10.0.15 (katso [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Uusi virhesanoma: Määrä ei kelpaa. Odotettiin %1 %2.

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Myyntilauksen hyllytystyön sijaintidirektiivien usean varastointiyksikön vaihtoehto ei arvioi usean sijaintidirektiivin toimintoja

### <a name="issue-description"></a>Ongelman kuvaus

*Myyntitilaus*-työtilaustyötyypin ja *Asetus*-työtyypin sijaintidirektiivit eivät arvioi usean sijaintidirektiivin toimintoja, kun **Useita varastointiyksiköitä** -vaihtoehto on valittu. Vain ensimmäinen sijaintidirektiivin toiminto arvioidaan.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Versioon 10.0.15 on lisätty uusi toiminto, *Arvioi kaikki usean varastointiyksikön sijaintidirektiivien toiminnot* (katso [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Tämä toiminto arvioi kaikki usean varastointiyksikön sijaintidirektiivien toiminnot. Jos tarvitse tätä toimintoa, ota se käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a>Varastonhallinnan mobiilisovellusta ei voi käyttää osittaiseen keräilyyn

### <a name="issue-description"></a>Ongelman kuvaus

Nimikkeiden ohittaminen ja osittainen keräily ei ole mahdollista myynti- ja siirtotilauksissa.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Määritä **Mobiililaitteen valikkovaihtoehdot** -sivulla jokaisen myynti- tai siirtotilausten käsittelyä varten määritetyn valikkovaihtoehdon **Salli työn jakaminen** -asetukseksi *Kyllä* **Yleiset**-välilehdellä.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Miten osittain määrän työn varaston tila muutetaan?

### <a name="issue-description"></a>Ongelman kuvaus

Haluat tehdä erän osittaisen määrän varaston tilan muutoksen.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varastonhallinnan mobiilisovellukseen voidaan luoda valikkovaihtoehto, jolla työntekijät voivat tehdä tämän muutoksen. Luo (tai muokkaa) **Mobiililaitteen valikkovaihtoehdot** -sivulla valikkovaihtoehto, jossa on seuraavat asetukset:

- **Tila:** *Työ*
- **Käytä aiemmin luotua työtä:** *Ei*
- **Työn luontiprosessi:** *Siirto*
- **Näytä varaston tila:** *Kyllä*

Sivulla voi määrittää tarvittaessa myös muita kenttiä.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Sijaintiprofiilin lähetys- ja vastaanottoalueen hallintaprofiili ei estä varastotyyppien sekoittamista.

### <a name="issue-description"></a>Ongelman kuvaus

Käytät *lähetyksen konsolidoinnin käytäntöjä*. Olet määrittänyt *lähetys- ja vastaanottoalueen hallintaprofiilin* *sijaintiprofiilille*, mutta kun töitä luodaan, lopullisessa sijainnissa on erilaisia varastotyyppejä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Lähetys- ja vastaanottoalueen hallintaprofiilit edellyttävät, että työt jaetaan etukäteen. Toisin sanoen lähetys- ja vastaanottoalueen hallintaprofiili odottaa, että työotsikolla ei ole useita asetussijainteja.

Jotta lähetys- ja vastaanottoalueen hallintaprofiili voisi hallita varastojen sekoittamista, on määritettävä työotsikon vaihto.

Tässä esimerkissä lähetys- ja vastaanottoalueen hallintaprofiili on määritetty siten, että **varastotyypit, joita ei pidä sekoittaa** on määritetty arvoon *Lähetystunnus*. Sitä varten määritetään työotsikon vaihto:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Valitse muokattava **Työtilauksen tyyppi** (kuten *Ostotilaukset*).
1. Valitse muokattava työmalli.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Avaa **Lajittelu**-välilehti ja lisää rivi seuraavin asetuksin:
    - **Taulukko** - *Väliaikaiset työtapahtumat*
    - **Johdettu taulukko** - *Väliaikaiset työtapahtumat*
    - **Kenttä** - *Lähetystunnus*
1. Valitse **OK**.
1. Palaat **Työmallit**-sivulle. Valitse toimintoruudussa **Työn otsikoiden katkaisut**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse **Kenttänimeen** *Lähetystunnus* yhdistetty valintaruutu.
1. Valitse toimintoruudussa **Tallenna**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

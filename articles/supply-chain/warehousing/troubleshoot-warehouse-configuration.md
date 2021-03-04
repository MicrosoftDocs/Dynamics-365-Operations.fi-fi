---
title: Varaston määrityksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä Microsoft Dynamics 365 Supply Chain Managementia määritettäessä.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646104"
---
# <a name="troubleshoot-warehouse-configuration"></a>Varaston määrityksen vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä Microsoft Dynamics 365 Supply Chain Managementia määritettäessä.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Seuraava virhesanoma avautuu: Rekisterikilpi tai sijainti ei kelpaa.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma avautuu,, kun rekisterikilven tunnus tai sijainti skannataan.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varmista, että mikään muu ei ole varannut rekisterikilven tunnusta. Tämä ongelma esiintyi aiemmin, kun käyttäjän varastosovelluksessa skannaama arvo oli sekä kelvollinen sijainti että kelvollinen rekisterikilven tunnus. Tämä ongelma kuitenkin korjattiin versiossa 10.0.11.

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

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>Varastosovellusta ei voi käyttää osittaiseen keräilyyn

### <a name="issue-description"></a>Ongelman kuvaus

Nimikkeiden ohittaminen ja osittainen keräily ei ole mahdollista myynti- ja siirtotilauksissa.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Määritä **Mobiililaitteen valikkovaihtoehdot** -sivulla jokaisen myynti- tai siirtotilausten käsittelyä varten määritetyn valikkovaihtoehdon **Salli työn jakaminen** -asetukseksi *Kyllä* **Yleiset**-välilehdellä.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Miten osittain määrän työn varaston tila muutetaan?

### <a name="issue-description"></a>Ongelman kuvaus

Haluat tehdä erän osittaisen määrän varaston tilan muutoksen.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varastosovellukseen voidaan luoda valikkovaihtoehto, jolla työntekijät voivat tehdä tämän muutoksen. Luo (tai muokkaa) **Mobiililaitteen valikkovaihtoehdot** -sivulla valikkovaihtoehto, jossa on seuraavat asetukset:

- **Tila:** *Työ*
- **Käytä aiemmin luotua työtä:** *Ei*
- **Työn luontiprosessi:** *Siirto*
- **Näytä varaston tila:** *Kyllä*

Sivulla voi määrittää tarvittaessa myös muita kenttiä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
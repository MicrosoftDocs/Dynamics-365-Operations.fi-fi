---
title: Tyhjä verotoimintoluettelo verolaskennan parametreissa
description: Tässä artikkelissa kuvataan sellaisen ongelman vianmääritystä, jossa veron laskentaparametrien sivun vero-ominaisuuksien luettelo on tyhjä.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 0d9286ec313a270da86181ff80ddfd690a757c9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869949"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Tyhjä verotoimintoluettelo verolaskennan parametreissa

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>Oire

Olet julkaissut Regulatory Configuration Servicessa (RCS) ominaisuuden, jotta voit käyttää sitä Microsoft Dynamics 365 Financessa. Kun kuitenkin avaat Financen, siirryt kohtaan **Vero** \> **Asetukset** \> **Verokonfiguraatio** \> **Verolaskennan parametrit**, ja yrität valita arvon **Ominaisuusmäärityksen nimi** -kentässä, arvojen luettelo on tyhjä.

## <a name="reason"></a>Syy

Tämä ongelma ilmenee yleensä siksi, että Finance-ympäristösi ja RCS-ympäristösi eivät ole samassa vuokraajassa.

### <a name="rcs-tenant"></a>RCS-vuokraaja

Noudattamalla näitä ohjeita voit etsiä RCS-vuokraajasi tunnuksen.

1. Kopioi koko RCS-URL-osoite. URL-osoite voi olla esimerkiksi `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Avaa InPrivate-selainikkuna, liitä RCS-URL-osoite osoitepalkkiin ja valitse **Enter**. Sinut ohjataan kirjautumissivulle, josta voit etsiä RCS-vuokraajan tunnuksen. Jos kirjautumissivun URL-osoite on esimerkiksi `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d`, vuokraajan tunnus on tieto, joka tulee näkyviin kohdan `https://login.microsoftonline.com/` jälkeen eli **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Finance-ympäristön vuokraajan tunnus

Voit etsiä Finance-ympäristön vuokraajan tunnuksen noudattamalla samoja ohjeita kuin minkä avulla RCS-vuokraaja löytyi. Kopioi ja liitä Finance-ympäristön täydellinen URL-osoite koko RCS-URL-osoitteen asemesta.

## <a name="resolution"></a>Ratkaisu

Jos nämä kaksi vuokraajatunnusta eroavat toisistaan, tässä artikkelissa kuvattu ongelma ilmenee. Jos ne ovat samoja, olet havainnut liittymättömiä ongelmia. Tässä tapauksessa suosittelemme, että otat yhteyttä Microsoft-tukeen.

### <a name="solution-1"></a>Ratkaisu 1

Kirjaa RCS-ympäristösi samalle vuokraajalle, johon Finance-ympäristö on kirjautunut. Luo ja julkaise sitten verotoiminto.

### <a name="solution-2"></a>Ratkaisu 2

Jaa verotoiminto Finance-vuokraajan kanssa RCS:ssä.

1. Siirry RCS:ssä kohtaan **Globalisointiominaisuudet** \> **Veronlaskenta**.
2. Valitse jaettava toiminto ja valitse sitten **Organisaatiot**-välilehdestä **Jaa seuraavan kanssa**.
3. Kirjoita **Organisaation toimialueen nimi**-kenttään nimi. For Kirjoita esimerkiksi **contoso.onmicrosoft.com**.
4. Valitse **Jaa**.

![Avattava Jaa ulkoisen organisaation kanssa -valintaikkuna.](media/ShareTaxFeature.png)

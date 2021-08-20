---
title: Uuden sähköisen laskutusominaisuuden luominen
description: Tässä aiheessa käsitellään uuden sähköisen laskutusominaisuuden luontia, kun omaa maata tai aluetta koskevaa valmista määritettävää ominaisuutta ei ole.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744932"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Uuden sähköisen laskutusominaisuuden luominen

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään uuden sähköisen laskutusominaisuuden luontia, kun omaa maata tai aluetta koskevaa valmista määritettävää ominaisuutta ei ole.

Uusi sähköinen laskutusominaisuus luodaan suorittamalla seuraavat tehtävät:

1. Uuden tiedostomuotomäärityksen luonti käyttämällä annettua laskumallimääritystä ja hyödyntämällä luotavan ominaisuuden nykyistä laskun yhdistämismääritystä.
2. Tiedostomuotomääritysten lisääminen sähköisen laskutusominaisuuden määrityksiin.
3. Sähköisen laskutusominaisuuden määrityksen luominen.
4. Uuden sähköisen laskutusominaisuuden viimeisteleminen ja julkaiseminen organisaation yleiseen säilöön.
5. Uuden sähköisen laskutusominaisuudet ottaminen käyttöön palveluympäristössä.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Nykyisestä laskumallista johdettujen uusien tiedostomuotomääritysten luominen

Tässä menettelyssä luodaan luotavassa uudessa sähköisessä laskutusominaisuudessa tarvittavat tiedostomuotomääritykset. Sähköisen laskun tiedostomuotomääritys ja mitkä tahansa muut tiedostomuotomääritykset, joita uusi sähköinen laskutusominaisuus voi tarvita, voidaan luoda.

Ennen menettelyn aloittamista on kirjauduttava Regulatory Configuration Service (RCS) -tilille.

1. Valitse Microsoft Dynamics 365 Financen **Sähköinen raportointi** -työtilassa **Microsoft**-määrityspalvelun **Säilöt**.
2. Valitse ensin **Yleinen**, sitten **Avaa** ja lopuksi vasemmassa ruudussa **Laskumalli**-määritys.

    > [!IMPORTANT]
    > Valitse Brasilian kohdassa sen sijaan **Veroasiakirjat**-mallimääritys.

3. Valitse **Määritykset**-välilehdessä **Tuo**.
4. Sulje sivu.
5. Sulje sivu.
6. Valitse **Raportointimääritykset**-ruutu ja valitse sitten tuotu laskumalli.
7. Valitse ensin **Luo määritys** ja sitten **Laskun kontekstimallin perustuva muoto**.
8. Anna muotomääritykselle nimi ja kuvaus.
9. Valitse **Muodon tyyppi**-kentässä tiedostotunnisteen tyyppi.
10. Valitse **Luo määritys** ja valitse luotu muotomääritys.
11. Valitse **Suunnitteluohjelma** ja määritä tiedostoasettelu muotoilun suunnittelutyökalulla siten, että se vastaa tiedostomuodon määrityksiä.
12. Sulje sivu.
13. Valitse **Versiot**-välilehdessä **Muuta tila** \> **Valmis**.
14. Julkaise muotomääritys yleiseen säilöön valitsemalla **Muuta tila** \> **Jaa**.

Uusi tiedostomuotomääritys on jaettava Microsoft-toimialueella, ennen kuin sähköinen laskutuspalvelu voi käyttää määritystä.

1. Valitse käytettävä muotomääritys. Määrityksen tilan on oltava **Jaettu**.
2. Valitse **Versiot**-välilehdessä **Jakamisen lisäasetukset** \> **Yleinen säilö**.
3. Valitse **Jaettu**-välilehdessä **Organisaatio**.
4. Jaa muotomääritys Microsoft-toimialueella antamalla **Parametrit**-kenttään **Microsoft.com**.
5. Valitse **OK**.

## <a name="create-the-new-electronic-invoicing-feature"></a>Uuden sähköisen laskutusominaisuuden luominen

1. Valitse RCS:ssä **Globalisaatio-ominaisuudet**-työtilan **Ominaisuudet**-osassa **Sähköinen laskutus** -ruutu.
2. Valitse ensin **Lisää** ja sitten **Uusi ominaisuus**.
3. Anna sähköisen laskutusominaisuuden nimi ja kuvaus
4. Valitse **Luo ominaisuus**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Sähköisen laskutuksen toiminnon määritysten lisääminen

1. Valitse käsittelyssä oleva sähköinen laskutusominaisuus.
2. Valitse **Määritykset**-välilehdessä **Lisää**.
3. Siirry **Määritykset**-ruudukossa tiedostomuotomäärityksiin ja valitse määritys, joka tarvitaan sähköisen laskutiedoston luontiin sähköisessä laskutusominaisuudessa.
4. Valitse **OK**.

## <a name="add-electronic-invoicing-feature-setups"></a>Sähköisen laskutusominaisuuden määritysten lisääminen

1. Valitse **Asetukset**-välilehdessä ensin **Lisää** ja sitten **Mukautettu asennus**.
2. Kirjoita ominaisuusmäärityksen nimi ja kuvaus.
3. Valitse **Määritystyyppi**-kentässä **Käsittelyputki**.
4. Valitse **Luo**.
5. Valitse käsittelyssä oleva määritys ja valitse sitten **Muokkaa**.
6. Lisää putkitoiminto valitsemalla **Käsittelyputki**-välilehdessä **Uusi**. Lisätietoja putkista on kohdassa [Toiminnot](e-invoicing-configuration-rcs.md#actions).
7. Lisää soveltuvuussääntölauseet valitsemalla **Soveltuvuussäännöt**-välilehdessä **Uusi**. Lisätietoja soveltuvuussäännöistä on kohdassa [Soveltuvuussäännöt](e-invoicing-configuration-rcs.md#applicability-rules).
8. Lisää tarvittavat muuttujat valitsemalla **Muuttujat**-välilehdessä **Uusi**.
9. Tarkista määrityksen yhdenmukaisuus valitsemalla ensin **Tallenna** ja sitten **Vahvista**.
10. Sulje sivu.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Sähköisen laskutusominaisuuden ottaminen käyttöön palveluympäristössä

Lisätietoja tämän tehtävän suorittamisesta on kohdassa [Sähköisen laskutusominaisuuden ottaminen käyttöön palveluympäristössä](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Sähköisen laskutusominaisuuden ottaminen käyttöön yhdistetyssä sovelluksessa

Lisätietoja tämän tehtävän suorittamisesta on kohdissa [Sovellusasetusten määrittäminen](e-invoicing-get-started.md#configure-the-application-setup) ja [Sähköisen laskutusominaisuuden ottaminen käyttöön yhdistetyssä sovelluksessa](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).

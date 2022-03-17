---
title: Globalisaatio-ominaisuuden luominen
description: Tässä ohjeaiheessa kerrotaan, miten voit luoda globalisaatio-ominaisuuden.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 197a5b983b307758425b1acc1f354d0a8bfbf8a1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371694"
---
# <a name="create-a-globalization-feature"></a>Globalisaatio-ominaisuuden luominen

[!include [banner](../includes/banner.md)]

Voit joko luoda sähköisen laskutuksen toiminnon tyhjästä tai pohjustaa sen aiemmin luotuun ominaisuuteen. Kun luot sähköisen laskutusominaisuuden tyhjästä, sinun on lisättävä sähköisen raportoinnin (ER) komponentit ja muut komponentit (kuten toimintoasetukset ja sovelluksen asetukset) manuaalisesti. Kun luot aiemmin luotuun toimintoon perustuvan ominaisuuden, uusi ominaisuus perii kaikki perusominaisuuden konfiguraatiot ja parametrit. Voit tarkistaa perusominaisuudesta uuteen ominaisuuteen kopioidut tiedot.

## <a name="create-a-feature-from-scratch"></a>Ominaisuuden luominen tyhjästä

Tässä osassa käsitellään sähköisen laskutusominaisuuden luontia, kun yleisessä tietovarastossa ei ole liiketoimintaasi sopivaa valmista globalisaatio-ominaisuutta.

Voit luoda sähköisen laskutuksen toiminnon noudattamalla seuraavia ohjeita.

1. Kirjaudu sisään Regulatory Configuration Service (RCS) -tilillesi.
2. Valitse **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Lisää** ja valitse sitten avattavasta valintaikkunasta **Uusi ominaisuus** -vaihtoehto.
4. Anna sähköisen laskutusominaisuuden nimi ja kuvaus.
5. Valitse **Luo ominaisuus**. Uuden ominaisuuden ensimmäinen versio näkyy sivun oikealla puolella, ja sen tila on **Luonnos**.

    Seuraavaksi on lisättävä ER-konfiguraatiot ja ominaisuusasetukset. Ennen kuin lisäät uusia tai aiemmin luotuja ER-muotokonfiguraatioita, varmista, että ne ovat paikallisessa RCS-tietovarastossa.

6. Valitse käsittelyssä oleva sähköinen laskutusominaisuus.
7. Valitse **Määritykset**-välilehdessä **Lisää**.
8. Etsi ja valitse **Konfiguraatiot**-ruudukossa muotokonfiguraatiot, joita käsittelyputki edellyttää (esimerkiksi sähköisten laskutiedostojen luomiseen tai ulkoisten Internet-palveluiden vastauksien käsittelyyn).
9. Valitse **OK**. Voit nyt käyttää konfiguraatioita käsittelyputken toiminnoissa. Lisätietoja on osiossa [Määritysten avulla työskentely](e-invoicing-work-configurations.md).
10. Voit lisätä sähköisen laskutusominaisuuden asetukset luomalla sen **Uusi ominaisuus** -sivun **Asetukset**-välilehdessä. Lisätietoja on kohdassa [Toimistoasetusten käsittely](e-invoicing-feature-setup.md).
11. Viimeistele määritys ja ota sähköinen laskutusominaisuus käyttöön palveluympäristössä. Lisätietoja: [Globalisaatio-ominaisuuden suorittaminen, julkaiseminen ja käyttöönottaminen](e-invoicing-complete-publish-deploy-globalization-feature).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Nykyisestä laskumallista johdettujen tiedostomuotomääritysten luominen

Voit ohittaa tämän osan, jos sinun ei tarvitse luoda ER-konfiguraatioita, mutta voit käyttää aiemmin luotuja versioita pohjana.

Tässä menettelyssä luodaan luotavassa uudessa sähköisessä laskutusominaisuudessa tarvittavat tiedostomuotomääritykset. Sähköisen laskun tiedostomuotomääritys ja mitkä tahansa muut tiedostomuotomääritykset, joita uusi sähköinen laskutusominaisuus voi tarvita, voidaan luoda.

1. Kirjaudu RCS-tilille.
2. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.
3. Valitse **Laskutusmalli** (tai Brasilian skenaarioille **Kirjanpitomalli**).
4. Valitse **Luo konfiguraatio** ja sitten avattavasta valintaikkunasta **Muoto, joka perustuu Lasku-tietomalliin** -vaihtoehto.
5. Anna muotomääritykselle nimi ja kuvaus.
6. Valitse **Muodon tyyppi**-kentässä tiedostotunnisteen tyyppi.
7. Valitse **Tietomallin määritys** -kentästä juurirakenne, jonne muoto yhdistetään. Esimerkiksi **InvoiceCustomer**-muotoa käytetään myyntilaskun muodoissa.
8. Valitse **Luo konfiguraatio**.
9. Valitse uusi muotokonfiguraatio.
10. Valitse **Suunnitteluohjelma** ja määritä tiedostoasettelu muotoilun suunnittelutyökalulla siten, että se vastaa tiedostomuodon määrityksiä.
11. Sulje sivu.
12. Valitse **Versiot**-välilehdessä **Muuta tila** \> **Valmis**.
13. Julkaise muotomääritys yleiseen säilöön valitsemalla **Muuta tila** \> **Jaa**.

Uudet tiedostomuotomääritykset on jaettava Microsoft-toimialueella, ennen kuin sähköinen laskutuspalvelu voi käyttää määritystä.

1. Valitse käytettävä muotomääritys. Määrityksen tilan on oltava **Jaettu**.
2. Valitse **Versiot**-välilehdessä **Jakamisen lisäasetukset** \> **Yleinen säilö**.
3. Valitse **Jaettu**-välilehdessä **Organisaatio**.
4. Jaa muotomääritys Microsoft-toimialueella antamalla **Parametrit**-kenttään **microsoft.com**.
5. Valitse **OK**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Aiemmin luotuun ominaisuuteen perustuvan ominaisuuden luominen

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
3. Varmista, että valitset aktiivisen tarjoajan **Konfiguraatiopalvelu**-kentässä. Näin uusi sähköinen laskutusominaisuus tulee näkyviin luettelossa sen luomisen jälkeen. Jos aktiivista konfiguraatiopalvelua ei ole valittu, uusi toiminto suodatetaan pois luettelosta.
4. Valitse **Lisää** ja valitse sitten avattavasta valintaikkunasta **Aiemmin luodun version perusteella** -vaihtoehto.
5. Kirjoita ominaisuuden nimi ja kuvaus.
6. Valitse **Perustoiminto**-kentästä ominaisuuden perusversio.
7. Valitse **Luo ominaisuus**. Ominaisuus luodaan, ja sen tila on **Luonnos**.
8. Tarkista ominaisuuksien osista, tarvitaanko päivityksiä:

    - Tarkista konfiguraatiot, jos sinun on mukautettava ER-muotoja ja niiden sidontaa ominaisuusversion muotokartoituksilla.
    - Tarkista asetukset, jos sinun on mukautettava **Toiminnot**-välilehteä, **Soveltuvuussäännöt**-välilehteä tai ominaisuusversion **Muuttujat**-välilehteä.

9. Viimeistele määritys ja ota sähköinen laskutusominaisuus käyttöön palveluympäristössä. Lisätietoja: [Globalisaatio-ominaisuuden suorittaminen, julkaiseminen ja käyttöönottaminen](e-invoicing-complete-publish-deploy-globalization-feature).

---
title: Projektimäärärahat
description: Tässä ohjeaiheessa kerrotaan, miten voit luoda tai muokata määrärahaa.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282824"
---
# <a name="project-grants"></a>Projektimäärärahat

[!include [banner](../includes/banner.md)]

Määräraha on tiettyyn tarkoitukseen tai projektiin liittyvä rahalahja. Määrärahan käyttämiseen liittyy tavallisesti rajoituksia. Projektinhallinta ja kirjanpito -kohdassa voit kirjoittaa ja seurata määrärahoja ja määrittää niiden suhteet projekteihin ja projektisopimuksiin. Voit esimerkiksi suorittaa seuraavat tehtävät:

- Liitä avustukset projekteihin ja rahoituslähteisiin **Projektin** ja **Projektisopimuksen tieto**-sivujen linkkien kautta.
- Kirjoita ja seuraa määrärahan liikkumista sen tilan muuttuessa.
- Kirjoita ja seuraa kustannuksia, pyydettyjä määriä ja myönnettyjä summia.
- Luo päämäärärahoja ja liitä niihin alimäärärahoja.

Voit luoda määrärahan kirjoittamalla kaikki tiedot uuteen tietueeseen tai voit kopioida ja muuttaa olemassa olevan määrärahan tietoja ja päivittää niitä.

## <a name="create-a-new-grant"></a>Luo uusi määräraha

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Määrärahat** \> **Määrärahat**.
2. Valitse **Uusi** \> **Määrärahat**.
3. Kirjoita avustuksen tiedot- sivun **Yleinen**-pikavälilehdellä **Avustuksen tunnus** -kenttään avustuksen aakkosnumeerinen tunnus.
4. Kirjoita määrärahan nimi **Määrärahan nimi** -kenttään.
5. Lisää **Kuvaus**-kenttään uuden määrärahan tiedot.

    Useimmat muista sivun kentistä ovat valinnaisia ja voit syöttää haluamasi määrän tietoja.

    Seuraavassa luettelossa kuvataan tiedot, jotka on määritetty määrärahan tiedot -sivun kussakin pikavälilehdessä:

    - **Yleinen** – Kirjoita määrärahan nimi, tila, kuvaus, tarkoitus ja määrä.
    - **Yhteystiedot** – Kirjoita määrärahaa hallitsevan henkilökunnan ja osaston tiedot ja tiedot määräraha-asiakkaasta tai organisaatiosta, joka on määrärahan lähde. Voit myös ilmaisee, onko organisaatiosi läpivientiyksikkö, joka vastaanottaa määrärahan ja välittää sen toiselle vastaanottajalle. Valitse **Lisää** lisätäksesi määrärahan antavan organisaation yhteystiedot, kuten puhelinnumerot ja sähköpostiosoitteet.
    - **Päivämäärät ja määräajat** – Kirjoita määrärahaan ja määrärahahakemukseen liittyvät päivämäärät. Esimerkkejä ovat hakemusten määräpäivä, lähetyspäivämäärä ja avustuksen hyväksymis- tai hylkäyspäivämäärä.
    - **Liitetyt projektit ja projektisopimukset** – Voit lisätä tähän pikavälilehteen tietoja vain, jos **yleinen** -pikavälilehden **avustuksen tila** -kentän arvoksi on määritetty **aktiivinen** tai **myönnetty**. Viimeistele liittyvä tehtävä valitsemalla seuraavista vaihtoehdoista:

        - **Lisää rahoituslähde** – Lisää määrärahalle uusi rahoituslähde. Voit kirjoittaa kaikki tiedot heti, tai käyttää oletusarvoisia tietoja ja sitten päivittää ne myöhemmin.
        - **Lisää projektisopimus** – Lisää tai päivitä projektisopimuksen tietoja.
        - **Lisää projekti** – Lisää tai päivitä projektitiedot.

    - **Määritys** – Määritä tiedot täsmäyttäviä rahastoja varten, jos nämä tiedot ovat pakollisia. Monet määrärahoja myöntävät yritykset vaativat vastaanottajia käyttämään määrätyn määrän omista rahoistaan tai resursseistaan vastaamaan myönnettyä määrärahan määrää. Voit määrittää **paikalliseen projekti- tai seurantatunnus** -kenttään tunnuksen, joka eroaa projektitunnuksesta.

        > [!NOTE]
        > Jos osa määrärahasta myönnetään eri organisaatiolle, aseta **Alimyöntäjä**-valinnaksi **Kyllä**. Yhdysvalloissa myönnetyille avustuksille voit määrittää, onko määräraha myönnetty valtion tai liittovaltion toimeksiantona.

    - **Vaihteluvälin tiedot** – Lisää tai päivitä tiedot siitä, kuinka usein myönnetyt määrärahat voidaan nostaa, laskuttaa tai käyttää.

## <a name="create-a-new-grant-from-a-copy"></a>Uuden avustuksen luominen kopiosta

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Määrärahat** \> **Määrärahat**.
2. Valitse **Uusi** \> **Kopioi määrärahasta**.
3. Kirjoita uudelle määrärahalle aakkosnumeerinen tunnus sekä nimi ja valitse sitten **OK**.
4. Tarkista kopioidun määrärahan tiedot ja tee tarvittavat muutokset määrärahan tiedot -sivulla. Useimmat sivun kentistä ovat valinnaisia.

## <a name="view-or-modify-grant-details"></a>Avustuksen tietojen tarkasteleminen tai muokkaaminen

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Määrärahat** \> **Määrärahat**.
2. Valitse muokattava määräraha.
3. Valitse toimintoruudun **Määräraha**-välilehden **Ylläpidä**-ryhmässä **Muokkaa**.
4. Tarkista määrärahan tiedot ja tee tarvittavat muutokset.

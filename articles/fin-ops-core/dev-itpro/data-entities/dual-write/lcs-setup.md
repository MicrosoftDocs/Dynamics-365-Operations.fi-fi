---
title: Kaksoiskirjoituksen asetukset Lifecycle Servicesistä
description: Tässä aiheessa käsitellään kaksoiskirjoitusyhteyden määrittämistä Microsoft Dynamics Lifecycle Servicesistä (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: df67e498b963af3ded7464f46f37bb4b2ca7d852
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127590"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Kaksoiskirjoituksen asetukset Lifecycle Servicesistä

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten kaksoiskirjoitusyhteys määritetään uuden Finance and Operations -ympäristön ja uuden Dataverse -ympäristön välille Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.

## <a name="prerequisites"></a>Edellytykset

Vain järjestelmänvalvoja voi määrittää kaksoiskirjoitusyhteyden.

+ Sinulla on oltava käyttöoikeus vuokraajaan.
+ Sinun on oltava järjestelmänvalvoja sekä Finance and Operations- että Dataverse -ympäristössä.

## <a name="set-up-a-dual-write-connection"></a>Kaksoiskirjoitusyhteyden määrittäminen

Näiden ohjeiden avulla voit määrittää kaksoiskirjoitusyhteyden.

1. Siirry LCS-sovelluksessa projektiin.
2. Ota uusi ympäristö käyttöön valitsemalla **Määritä**.
3. Valitse versio. 
4. Valitse topologia. Jos käytettävissä on vain yksi topologia, se valitaan automaattisesti.
5. Suorita ensimmäiset vaiheet ohjatussa **Käyttöönoton asetukset** -toiminnossa.
6. Tee jokin seuraavista vaiheista **Dataverse** -välilehdessä:

    - Jos Dataverse -ympäristö on jo valmisteltu vuokraajaa varten, voit valita sen.

        1. Määritä **Määritä Dataverse** -asetuksen arvoksi **Kyllä**.
        2. Valitse **Käytettävissä olevat ympäristöt** -sarakkeessa Finance and Operations -tietojen kanssa integroitava ympäristö. Luettelo sisältää kaikki ympäristöt, joiden järjestelmänvalvojan oikeudet sinulla on.
        3. Valitse **Hyväksyn**-valintaruutu, jolloin hyväksyt ehdot.

        ![Dataverse -välilehti, kun Dataverse -ympäristö on jo valmisteltu vuokraajaa varten](../dual-write/media/lcs_setup_1.png)

    - Jos vuokraajalla ei vielä ole Dataverse -ympäristöä, uusi ympäristö valmistellaan.

        1. Määritä **Määritä Dataverse** -asetuksen arvoksi **Kyllä**.
        2. Anna Dataverse -ympäristön nimi.
        3. Valitse alue, johon ympäristö otetaan käyttöön.
        4. Valitse ympäristön oletuskieli ja -valuutta.

            > [!NOTE]
            > Et voi muuttaa kieltä ja valuuttaa myöhemmin.

        5. Valitse **Hyväksyn**-valintaruutu, jolloin hyväksyt ehdot.

        ![Dataverse -välilehti, kun vuokraajalla ei ole Dataverse -ympäristöä](../dual-write/media/lcs_setup_2.png)

7. Suorita jäljellä olevat vaiheet ohjatussa **Käyttöönoton asetukset** -toiminnossa.
8. Kun ympäristön tila on **Otettu käyttöön**, avaa ympäristön tietojen sivu. **Power Platform -integrointi** -osassa on linkitettyjen Finance and Operations- ja Dataverse -ympäristöjen nimet.

    ![Power Platform -integrointi -osa](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations -ympäristön järjestelmänvalvojan on kirjauduttava sisään LCS-sovellukseen ja valittava **Linkitä CDS for Apps -sovellukseen**, jotta linkitys on valmis. Ympäristön tietojen sivulla näkyvät järjestelmänvalvojan yhteystiedot.

    Kun linkki on valmis, tilaksi päivitetään **Ympäristön linkitys on suoritettu onnistuneesti**.

10. Voit avata **Tietojen integrointi** -työtilan Finance and Operations -ympäristössä ja hallinnoida käytettävissä olevia malleja valitsemalla **Linkitä CDS for Apps -sovellukseen**.

    ![Linkitä CDS for Apps --painike Power Platform -integrointi -osassa](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Et voi poistaa ympäristöjen välistä linkitystä LCS-sovelluksen avulla. Jos haluat poistaa linkityksen, avaa **Tietojen integrointi** -työtila Finance and Operations -ympäristössä ja valitse sitten **Poista linkitys**.


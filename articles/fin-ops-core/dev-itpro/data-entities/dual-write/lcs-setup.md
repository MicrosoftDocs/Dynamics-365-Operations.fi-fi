---
title: Kaksoiskirjoituksen asetukset Lifecycle Services -sovelluksessa
description: Tässä ohjeaiheessa kerrotaan, miten kaksoiskirjoitusyhteys määritetään uuden Finance and Operations -ympäristön ja uuden Dataverse -ympäristön välille Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.
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
ms.openlocfilehash: 25db9c58c3d09e44dcf11b48cae1a9eda4241c35
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683521"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Kaksoiskirjoituksen asetukset Lifecycle Services -sovelluksessa

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

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
        2. Valitse **Käytettävissä olevat ympäristöt** -kentässä Finance and Operations -tietojen kanssa integroitava ympäristö. Luettelo sisältää kaikki ympäristöt, joiden järjestelmänvalvojan oikeudet sinulla on.
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
8. Kun ympäristön tila on **Otettu käyttöön**, avaa ympäristön tietojen sivu. **Dataverse -ympäristön tiedot** -osassa on linkitettyjen Finance and Operations- ja Dataverse -ympäristöjen nimet.

    ![Dataverse -ympäristön tietojen osa](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations -ympäristön järjestelmänvalvojan on kirjauduttava sisään LCS-sovellukseen ja valittava **Linkitä CDS for Apps -sovellukseen**, jotta linkitys on valmis. Ympäristön tietojen sivulla näkyvät järjestelmänvalvojan yhteystiedot.

    Kun linkki on valmis, tilaksi päivitetään **Ympäristön linkitys on suoritettu onnistuneesti**.

10. Voit avata **Tietojen integrointi** -työtilan Finance and Operations -ympäristössä ja hallinnoida käytettävissä olevia malleja valitsemalla **Linkitä CDS for Apps -sovellukseen**.

    ![Linkitä CDS for Apps -sovellukseen -painike Dataverse -ympäristön tietojen osassa](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Et voi poistaa ympäristöjen välistä linkitystä LCS-sovelluksen avulla. Jos haluat poistaa linkityksen, avaa **Tietojen integrointi** -työtila Finance and Operations -ympäristössä ja valitse sitten **Poista linkitys**.

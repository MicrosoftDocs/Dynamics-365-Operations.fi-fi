---
title: Arvonlisäveromaksun luominen
description: Tilitys- ja arvonlisäveron kirjaustyö tilittävät arvonlisäverosaldot arvonlisäverotileille ja tekee niistä vastakirjauksen kyseisen kauden arvonlisäveron tilitystilille.
author: twheeloc
ms.date: 10/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54132ca4775482b4a06ff7e73125e804aff40cb4
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700110"
---
# <a name="create-a-sales-tax-payment"></a>Arvonlisäveromaksun luominen

[!include [banner](../../includes/banner.md)]

Tilitys- ja arvonlisäveron kirjaustyö tilittävät arvonlisäverosaldot arvonlisäverotileille ja tekee niistä vastakirjauksen kyseisen kauden arvonlisäveron tilitystilille.

1. Siirry kohtaan **Vero > Ilmoitukset > Arvonlisävero > Tilitä ja kirjaa arvonlisävero**.
2. Avaa haku valitsemalla **Tilityskausi**-kentässä avattavan valikon painike.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Syötä päivämäärä **Päivämäärästä**-kenttään.
    - Jos **Sisällytä korjaukset** -vaihtoehtoa ei ole valittu **Kirjanpidon parametri** -sivulla, tilitystä ei voi suorittaa eri versioille. Alkuperäinen on kausivälin ensimmäinen tilitys. Se voidaan käsitellä vain kerran kausivälin aikana. Uusimmat korjaukset tilittävät arvonlisäverotapahtumat, jotka on kirjattu alkuperäisen version luomisen jälkeen.
5. Syötä **Tapahtumapäivä**-kenttään päivämäärä.
6. Valitse **OK**.

## <a name="performance-consideration"></a>Suorituskyvyn osalta huomioon otettavaa

Arvonlisäveron maksumenettelyn valmistuminen voi kestää kauan. Keskeisimmät menettelyn suorittamiseen vaikuttavat tekijät ovat tilityskauden laskujen määrä sekä niiden merkintöjen määrä, jotka on kirjattava arvonlisäveron tilitystositteeseen. Voit parantaa suorituskykyä ohittamalla toimintoja, joita ei tarvita prosessissa.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Arvonlisäveron maksamisen suorituksen parantamisen ominaisuuden käyttöönotto

**Arvonlisäverojen maksumenettely** -ominaisuus voi auttaa arvonlisäveron maksumenettelyn suorittamisen parantamisessa siten, että se kokoaa yhdelle arvonlisäveron maksutositteen riville kirjanpitovaluutan määrän ja vastaavan valuutan määrän arvonlisäveron maksulomakkeen riveille, jolla on sama päätili, kirjanpitodimensio ja valuutta.

1. Valitse **Järjestelmänvalvoja** \> **Työtilat** \> **Ominaisuuksien hallinta**.
2. Hae **Kaikki**-välilehdessä **Arvonlisäveron maksamisen suorituksen parantaminen** ja valitse se.
3. Valitse **Ota käyttöön**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Verotapahtumien vastakirjauksien luonnin estäminen

Oletusarvoisesti arvonlisäveron maksutosite kirjaa vastakirjauksen jokaisen sellaisen arvonlisäverotapahtuman osalta, joka tilitetään arvonlisäveron maksumenettelyssä. Arvonlisäveron vastakirjaustapahtumat sisältyvät **Arvonlisäveron/kirjanpidon täsmäytys** -raporttiin. Ne näyttävät niiden arvonlisäverotapahtumien saldon, joita ei tilitetä jakson aikana.

Arvonlisäveron vastatapahtumat voivat kuitenkin lisätä arvonlisäveron maksumenettelyn rasitetta. Siksi **TaxReportGenOffsetTaxTransPerRecordSetFlighting**-niminen väliversiotestaus voidaan ottaa käyttöön tarpeen mukaan. Tämä väliversiotestaus voi parantaa veron vastatapahtuman luomista maissa ja alueilla Thaimaata, Puolaa, Unkaria, Liettuaa, Malesiaa, Intiaa, Italiaa, Venäjää, Tšekin tasavaltaa, Viroa ja Latviaa lukuun ottamatta.

> [!NOTE]
> Jos verotapahtumataulukossa on mukautettuja kenttiä, väliversiotestausta ei voi ottaa käyttöön.

Koska **Arvonlisäveron/kirjanpidon täsmäytys** -raporttia käytetään yleensä vain sisäisen valvonnan tarkoituksiin ja sitä ei vaadita monissa verojärjestelmissä, voit jättää luomatta arvonlisäveron vastakirjaustapahtumia arvonlisäveron maksutositteessa.

1. Siirry kohtaan **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäveron tilityskaudet**.
2. Valitse tilityskausi.
3. Määritä **Yleistä**-pikavälilehdessä **Estä verotapahtumien vastakirjauksien luonti** -asetuksen arvoksi **Kyllä**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: "Taloushallinnon dimensioiden lisääminen talousjohtajan työtilaan"
description: "Tässä ohjeaiheessa kerrotaan, miten taloushallinnon dimensiot lisätään talousjohtajan työtilaan siten, että niitä voi käyttää kirjapito- ja budjettiraporteissa."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: fi-fi
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Taloushallinnon dimensioiden lisääminen talousjohtajan työtilaan

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten taloushallinnon dimensiot lisätään talousjohtajan työtilaan siten, että niitä voi käyttää kirjapito- ja budjettiraporteissa. Talousjohtajan työtilassa on **Yleiskatsaus**- ja **Taloushallinto**-välilehdet. Näiden välilehtien raportit perustuvat kahteen mittaan: LedgerActivityMeasure ja BudgetActivityMeasure. Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin heinäkuun 2017 päivityksessä näiden kahden mitan ja DimensionCombinationEntity-yksikön välillä on suhde. Tämän vuoksi dimensiot voidaan valita.

1. Päivitä Finance and Operationsin **Yksikkösäilö**-sivulla **LedgerActivityMeasure**- ja **BudgetActivityMeasure**-mitat.
2. Avaa Microsoft Visual Studiossa Application Explorer ja tee haku hakusanalla **LedgerCFO**.
3. Avaa **Resurssit**-kohdassa **LedgerCFOWorkspacePBIX**.
4. Kun resurssi avautuu Microsoft Power BI Desktopissa, valitse ensin **Nouda tiedot**, sitten **SQL Server -tietokanta** ja lopuksi **Yhdistä**.
5. Anna ensin palvelimen nimi ja sitten tietokannaksi **AxDW**. Valitse ensin **DirectQuery** ja sitten **OK**.
6. Etsi ja valitse **LedgerActivityMeasure\_DimensionCombination** ja valitse sitten **Lataa**.

    > [!TIP]
    > Vaihda taulun nimeksi **Kentät**-luettelossa **Taloushallinnon dimensiot**, jotta se on helppo tunnistaa.

7. Valitse ensin **Suhteiden hallinta** ja sitten **Uusi**.
8. Valitse ensin ensimmäisessä kentässä **Kirjanpitotehtävät** ja sitten **LedgerDimension**.
9. Valitse toisessa kentässä **LedgerActivityMeasure\_DimensionCombination** (tai **Taloushallinnon dimensiot**, jos muutit kentän nimen). Valitse **DimensionCombinationRECID**-otsikko.
10. Valitse **Kardinaliteetti**-kentässä **Monta yhteen**.
11. Vaihda **Ristisuodatus**-arvoksi **Yksittäinen**.
12. Valitse ensin sekä **Tee tästä suhteesta aktiivinen** että **Oleta viite-eheys**, sitten **OK** ja lopuksi **Sulje**.

    [![Suhteen luominen](./media/Create-relationship.png)](./media/Create-relationship.png)

13. **Kentät**-luettelossa pitäisi olla taulu ja käytettävissä olevat taloushallinnon dimensiot. Vedä sopivat taloushallinnon dimensiot raporttitason suodattimiin.
14. Tallenna muutokset.
15. Napsauta sovellusobjektipuussa (AOT) hiiren kakkospainikkeella projektia ja valitse sitten **Synkronoi**.
16. Luo projekti ja tarkastele sitten tuloksia avaamalla sovellus.

    [![Valmis työtila](./media/workspace.png)](./media/workspace.png)


---
title: Varastokirjauskansioiden avattavaa Työnkulku-valintaikkunaa ei löydy
description: Avattavaa Työnkulku-valintaikkunaa ei ole kirjauskansiosivulla tai liittyvät työnkulkutoiminnot eivät ole käytettävissä
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476210"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Varastokirjauskansioiden avattavaa Työnkulku-valintaikkunaa ei löydy

## <a name="symptoms"></a>Oireet

Avattavaa **Työnkulku**-valintaikkunaa ei ole kirjauskansiosivulla tai liittyvät työnkulkutoiminnot eivät ole käytettävissä.

Ongelman esiintymiselle on kolme syytä, jotka käsitellään seuraavissa kohdissa.

## <a name="resolution-1"></a>Ratkaisu 1

Jos ongelma koskee kaikki käyttäjiä, syynä voi olla se, että hyväksynnän työnkulkua ei ole määritetty kyseiselle kirjauskansiolle. Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Valitse **Varastonhallinta &gt; Asetukset &gt; Kirjauskansioiden nimet &gt; Varasto**.
1. Valitse luetteloruudussa kirjauskansion nimi ja avaa kirjauskansion asetukset.
1. Määritä **Yleinen**-pikavälilehdessä **Hyväksyntätyönkulku** -asetukseksi *Kyllä*. Jos järjestelmä pyytää vahvistamaan muutoksen, valitse **Kyllä**.
1. Valitse **Työnkulku**-kentässä työnkulku, jota haluat käyttää valitussa kirjauskansiossa.

## <a name="resolution-2"></a>Ratkaisu 2

Jos työnkulku käyttää mukautettua koodia, ongelmia voi esiintyä järjestelmän päivityksen jälkeen. Esimerkiksi **Lähetä**-painike näkyy kirjauskansion työnkulussa harmaana, joten lähetystä ei voi hyväksyä painikkeen valinnalla.

Jos **Lähetä**-painike näkyy harmaana, työnkulkua on ehkä mukautettu. Tämä tarkoittaa sitä, että työnkulun menetelmää `canSubmitToWorkflow()` kohdassa `FormDataUtil` on laajennettu. Tämä ongelma korjataan muuttamalla tapaa, jolla `canSubmitToWorkflow()`-menetelmä laajennetaan käyttämään rakennetta seuraavassa esimerkissä.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Ratkaisu 3

Jos ongelma koskee vain muutamia käyttäjiä, kyseisillä käyttäjillä ei ehkä ole suojausoikeuksia, joita tarvitaan työnkulkutoimintojen suorittamiseen varastokirjauskansioissa. Varmista, että kullakin käyttäjällä, joita on ongelma koskee, on *Ylläpidä varastokirjauskansion työnkulkua* -suojausoikeus. Tämä oikeus määritetään oletusarvoisesti velvollisuudelle, jolla on sama nimi, ja kyseistä velvollisuutta käytetään *Varastotyöntekijä*- ja *Varastopäällikkö*-rooleissa.

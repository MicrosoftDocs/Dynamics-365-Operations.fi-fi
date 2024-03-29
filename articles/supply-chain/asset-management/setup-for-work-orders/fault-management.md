---
title: Vikojen hallinta
description: Tässä artikkelissa kerrotaan vikojen hallinnasta resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 10a4a209b54aa31c4a2f6970f46ab8b1a2cbef97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874156"
---
# <a name="fault-management"></a>Vikojen hallinta

[!include [banner](../../includes/banner.md)]

 

Käyttöomaisuuden hallinnassa voit käyttää vian suunnittelua käyttöomaisuustyyppien vian oireiden, vika-alueiden ja vikatyyppien määrittämiseen. Näin voit hallita käyttöomaisuudessa havaittuja virheitä. Lisäksi vian syyt ja virheiden korjausehdotukset voidaan kirjata työtilaukseen.

Virheiden rekisteröintiä ja hallintaa koskeva prosessi koostuu näistä vaiheista.

1. Luo luettelo vikaoireista, vika-alueista ja vikatyypeistä, joita voi ilmetä käyttöomaisuustyypeissä.
2. Määritä vian suunnittelussa oireet, vika-alueet ja vikatyypit.

Seuraavassa on joitakin esimerkkejä, joiden avulla voit ymmärtää vian oireiden, vika-alueiden ja vikatyyppien välisen eron.

**Vikojen oireet:**

- Epäsymmetriset jännitteet
- Oikosulku
- Melu
- Vuoto
- Tärinä

**Vika-alueet:**

- Sähköinen
- Mekaaninen
- Hydraulinen
- Pneumaattinen

**Vikatyypit:**

- Viallinen päästaattorin käämitys
- Viallinen diodi
- Likaiset käämit
- Viallinen generaattori
- Viallinen anturi

## <a name="create-fault-symptoms"></a>Vikojen oireiden luominen

Noudattamalla näitä ohjeita voit luoda luettelon oireista, joita voidaan käyttää vian suunnittelutoiminnossa.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vikojen oireet**.
2. Luo tietue valitsemalla **Uusi**.
3. Kirjoita **Vikojen oireet** -kenttään vian oireen nimi.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse **Tallenna**.

## <a name="create-fault-areas"></a>Vika-alueiden luominen

Noudattamalla näitä ohjeita voit luoda luettelon alueista tai sijainneista, joita voidaan käyttää vian suunnittelutoiminnossa.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vika-alueet**.
2. Luo tietue valitsemalla **Uusi**.
3. Kirjoita **Vika-alue** -kenttään vika-alueen nimi.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse **Tallenna**.

## <a name="create-fault-types"></a>Luo vikatyypit

Noudattamalla näitä ohjeita voit luoda luettelon vikatyypeistä, joita voidaan käyttää vian suunnittelutoiminnossa.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vikatyypit**.
2. Luo tietue valitsemalla **Uusi**.
3. Syötä **Vikatyyppi**-kenttään vikatyypin nimi.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse **Tallenna**.

## <a name="set-up-the-fault-designer"></a>Vian suunnittelutoiminnon määrittäminen

Vian suunnittelussa määritetään käyttöomaisuustyyppien vikatiedot.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian suunnittelutoiminto**.
2. Valitse vasemmanpuoleisesta ruudusta käyttöomaisuustyyppi, jolle haluat määrittää vikatietueen.
3. Valitse **Vian oire** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vian oire-** kentästä vian oire.
4. Valitse **Vika-alue** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vika-alue** -kentästä vian oire.
5. Valitse **Vikatyyppi** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vikatyyppi** -kentästä vikatyyppi.
6. Voit luoda nopeasti kaikkien aiemmin luotujen vian oireiden, vika-alueiden ja vikatyyppien yhdistelmiä valitun käyttöomaisuustyypin osalta valitsemalla **Luo vikayhdistelmät**. Tämä toiminto on hyödyllinen, jos olet lisännyt useita vian oireita, vika-alueita ja vikatyyppejä. On helpompaa poistaa niiden yhdistelmien rivit, jotka eivät liity käyttöomaisuuslajiin, kuin luoda uusia rivejä manuaalisesti.

    > [!NOTE]
    > Jos haluat kopioida vian oireiden, -alueiden ja -tyyppien määritykset yhdestä käyttöomaisuuslajista valittuun käyttöomaisuustyyppiin, valitse **Kopioi resurssityypistä**.

7. Tallenna muutokset valitsemalla **Tallenna**.

![Vian suunnittelutoimintosivu.](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Luo vian syyt

Seuraavien vaiheiden avulla voit luoda luettelon tunnetuista vikojen syistä, jotka voidaan lisätä työtilaukseen tai ylläpitopyyntöön.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian syyt**.
2. Luo tietue valitsemalla **Uusi**.
3. Syötä **Vian syy**-kenttään vian syyn nimi.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse **Tallenna**.

## <a name="create-fault-remedies"></a>Vian korjaustoimenpiteiden luominen

Seuraavien vaiheiden avulla voit luoda luettelon korjausehdotuksista, jotka voidaan lisätä työtilaukseen tai ylläpitopyyntöön.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian korjaukset**.
2. Luo tietue valitsemalla **Uusi**.
3. Kirjoita **Vian korjaus** -kenttään vian korjauksen nimi.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse **Tallenna**.

> [!NOTE]
> Voit muuttaa vian oireiden, alueiden, tyyppien, syiden ja korjaustoimenpiteiden nimiä tarpeen mukaan. Nimen muutokset näkyvät automaattisesti liittyvissä vikarekisteröinneissä.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
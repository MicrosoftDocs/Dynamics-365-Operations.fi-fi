---
title: Visualisoinnin ja yhteistyön toteutus
description: Tässä artikkelissa käsitellään DDMRP:n (kysyntäperustaisen materiaalitarvesuunnittelun) erotuspisteitä, puskurivyöhykkeitä, suunniteltuja tilauksia ja historiatietoja.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: e3afdd10860494b3cfe73a113a0e4e8fb07682a1
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186669"
---
# <a name="visual-and-collaborative-execution"></a>Visualisoinnin ja yhteistyön toteutus

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Tässä artikkelissa käsitellään DDMRP:n (kysyntäperustaisen materiaalitarvesuunnittelun) erotuspisteitä, puskurivyöhykkeitä, suunniteltuja tilauksia ja historiatietoja.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Valitun nimikkeen puskureiden ja määrien visuaalinen seuranta

Microsoft Dynamics 365 Supply Chain Managementissa voidaan seurata visuaalisesti puskureita, varastosaldoja ja nettovuotasojen muutoksia ajankulussa minkä tahansa valitun vapautetun tuotteen osalta. Kaaviot voidaan avata ja niitä voidaan tarkastella seuraavien ohjeiden avulla.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse erotuspisteeksi määritetty vapautettu nimike. (Lisätietoja on kohdassa [Varaston asemointi](ddmrp-inventory-positioning.md).)
1. Valitse toimintoruudun **Suunnitelma**-välilehdessä **Nimikekattavuus**.
1. Valitse **Nimikkeen kattavuus** -sivulla erotuspisteen luova nimikkeen kattavuustietue. (Tämä tietue näyttää erotuspisteet luomaan määritetyn kattavuusryhmän nimen.)
1. Valitse **Varastosaldo**-välilehti. Tässä välilehdessä on kaavio, joka näyttää varastosaldon määrien muuttumisen ajan mittaan sekä tietylle ajanjaksolle kirjatun varastosaldotason aina, kun kyseinen suunnittelun optimointi suoritetaan. Välilehdessä on myös taulukko, josta näkee, mihin seuraavista luokista kukin kirjattu varastosaldotaso kuuluu:

    - **Kriittisen vähissä** – alle puolet jakson vähimmäismäärästä.
    - **Alhainen** – sijoittuu vähimmäismäärän puolikkaan ja vähimmäismäärän väliin.
    - **Keskimääräinen käytettävissä oleva varasto** – vähimmäismäärän sekä vähimmäismäärän ja vihreän vyöhykkeen välissä.
    - **Keskimääräistä suurempi** – keskimääräistä suurempi.

    ![Historialliset varastotasot Varastotaso-välilehdessä](media/ddmrp-on-hand-graph.png "Historialliset varastotasot Varastotaso-välilehdessä")

    > [!NOTE]
    > **Varastosaldo**-välilehdessä käytettävät värit ilmaisevat eri alueita kuin **Puskuriarvot**-välilehdessä käytettävät samankaltaiset värit.

1. Puskuriarvojen aja mittaan tapahtunutta muutosta sekä niiden vertailua varastosaldon ja nettovirran tasoihin voi tarkastella valitsemalla **Puskuriarvot**-välilehden.

    ![Historialliset varastosaldo- ja nettovirtatasot Puskuriarvot-välilehdessä](media/ddmrp-buffer-values-graph.png "Historialliset varastosaldo- ja nettovirtatasot Puskuriarvot-välilehdessä")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Kaikkien erotuspisteiden tilan ja suunniteltujen tilausten seuraaminen

**Kysyntään perustuva MRP** -työtilassa on useita työkaluja sekä erotuspistenimikkeiden ja liittyvien suunniteltujen tilausten tilan tunnuslukuja ja yleiskatsauksia. Avaa se valitsemalla **Pääsuunnittelu \> Työtilat \> Kysyntään perustuva MRP**.

![Kysyntään perustuva MRP -työtila](media/ddmrp-workspace.png "Kysyntään perustuva MRP -työtila")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Erotuspisteiden ja suunniteltujen tilausten yleiskatsausten hakeminen

**Kysyntään perustuva MRP** -työtilan lisäksi Supply Chain Managementissa on useita sivuja, joissa voi tarkastella DDMRP-määrityksiä, erotuspisteitä ja suunniteltuja tilauksia koskevia tietoja. Joillakin näistä sivuista on toimintoruudussa käteviä painikkeita, joilla voi hallita puskureita, suorittaa pääsuunnittelun ja avata muita liittyviä näkymiä.

- Nettovirtatason mukaista erotuspisteen tilaa voi tarkastella valitsemalla **Pääsuunnittelu \> Pääsuunnittelu \> DDMRP \> Erotuspisteiden tila nettovirran mukaan**.
- Käytettävissä olevan varaston mukaista erotuspisteen tilaa voi tarkastella valitsemalla **Pääsuunnittelu \> Pääsuunnittelu \> DDMRP \> Erotuspisteiden tila käytettävissä olevan varaston mukaan**.
- Erotuspisteiden suunniteltuja tilauksia voi tarkastella valitsemalla **Pääsuunnittelu \> Pääsuunnittelu \> DDMRP \> Erotuspisteiden suunnitellut tilaukset**.
- Erotettuja läpimenoaikoja voi tarkastella valitsemalla **Pääsuunnittelu \> Pääsuunnittelu \> DDMRP \> Erotettu läpimenoaika**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Erotuspisteen puskuriarvojen tyhjentäminen

Järjestelmään kertyy ajan mittaan suuri määrä meneillään oleviin puskurilaskelmiin liittyviä historiallisia tietoja. Nämä historialliset tiedot lisäävät tietomäärää, mikä voi vaikuttaa ajan kuluessa järjestelmän suorituskykyyn. Tämän vuoksi on suositeltavaa, että vanhat erotuspisteiden puskuriarvot tyhjennetään ajoittain.

> [!WARNING]
> Tyhjennystyö poistaa historialliset puskuriarvoasetukset sekä historialliset varastosaldo ja nettovirtatiedot. Näitä tietoja ei voi palauttaa.

Erotuspisteen puskuriarvot tyhjennetään seuraavien ohjeiden mukaisesti.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> DDMRP \> Tyhjennä erotuspisteen puskuriarvot**.
1. Määritä **Tyhjennä erotuspisteen puskuriarvot** -valintaikkunassa seuraavat kentät:

    - **Poista tietueet, jotka ovat vanhempia kuin (päivinä)** – Määritä uusimpien säilytettävien tietojen ikä päivinä. Kaikki tätä arvo vanhemmat erotuspisteen puskuriarvot poistetaan.
    - **Pääsuunnitelma** – Valitse pääsuunnitelma, joka sisältämiin nimikkeisiin tyhjennyksellä on vaikutusta. Tyhjennys koskee kaikki suunnitelman nimikkeitä sen jälkeen, kun tässä ikkuna määritettyjä **Suodatus**-asetuksia käytetään.

1. Kyseiseen suoritettavaan erätyöhön sisältyviä tietueita voi rajoittaa avaamalla **Kysely**-valintaikkuna valitsemalla **Suodatus** **Sisällytettävät tietueet**-pikavälilehdessä. Valintaikkuna toimii samalla tavalla kuin muissakin Supply Chain Managementin [taustatöissä](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).
1. Määritä **Suorita taustalla** -pikavälilehdessä, miten, milloin ja kuinka usein tyhjennys tehdään. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Lisää uusi työ eräjonoon suoritettavaksi valitsemalla **OK**.

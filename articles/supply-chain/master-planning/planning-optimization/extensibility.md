---
title: Suunnittelun optimoinnin laajennettavuus
description: Tässä artikkelissa kuvataan suunnittelun optimoinnin tukemat laajennettavuusskenaariot.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857541"
---
# <a name="planning-optimization-extensibility"></a>Suunnittelun optimoinnin laajennettavuus

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan suunnittelun optimoinnin tukemat ja pääsuunnitteluun liittyvät laajennettavuusskenaariot. Nämä pilvipohjaiset ominaisuudet ovat saatavilla Microsoft Dynamics 365 Supply Chain Managementin versiosta 10.0.13 alkaen.

## <a name="custom-processing-when-master-planning-is-completed"></a>Mukautettu käsittely, kun pääsuunnittelu on valmis

Suunnittelun optimoinnin yleisimmässä laajennettavuusskenaariossa, mukautettu käsittely suoritetaan, kun suunnitelma on päivitetty. Voit esimerkiksi lisätä sarakkeen suunniteltujen tilausten taulukkoon (`ReqPO`) tai johtaa tilastotietoja luodusta suunnitelmasta. Pääasiallinen laajennettavuuspiste, joka mahdollistaa nämä skenaariot on `MpsMasterPlanningEvents`-luokan `jobCompletedSuccessfully`-menetelmä.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Tässä on esimerkki laajennuksesta, joka määrittää suunnitellussa tilauksessa mukautetun `CstmOrderPriority`-kentän.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Kun lisäät mukautetun logiikan, ota huomioon seuraavat rajoitukset ja parhaat käytännöt:

- Menetelmä `jobCompletedSuccessfully` kutsutaan tapahtuman laajuuden ulkopuolella. Siten suunnitelma näkyy käyttäjälle jo, kun mukautetun logiikan suorittaminen alkaa. Jos mukautus määrittää ylimääräisiä kenttiä suunniteltuihin tilauksiin, on tärkeää ilmoittaa käyttäjille, että näiden kenttien arvot ovat lopulta yhdenmukaisia (eli ne saattavat olla vanhentuneita heti suunnittelutyön valmistumisen jälkeen).
- Toinen pääsuunnittelun työ voi alkaa, kun `jobCompletedSuccessfully`-menetelmä kutsutaan. Uusi työ saattaa vaikuttaa koko suunnitelmaan tai suunnitelman osaan. Uusi työ saattaa päivittää tai poistaa samat suunnitellut tilaukset tai tarvetapahtumat, jotka on luotu tai päivitetty osana suunnittelutyötä, joka on käsiteltiin `jobCompletedSuccessfully`-menetelmässä. Päivityksen ristiriitapoikkeuksen on käsiteltävä, kun tämä tapahtuma laajennetaan.
- Vältä yksittäistä tapahtumalaajuutta, kun laajennat tämän menetelmä. Yksi pääsuunnittelusuoritus voi tuottaa miljoonia tarvetapahtumia ja tuhansia suunniteltuja tilauksia. Jos kaikki nämä tapahtumat ja suunnitellut tilaukset käsitellään yksittäisen tapahtuman puitteissa, ilmenee useita SQL-lukituksia, jotka estävät muita suunnitteluprosesseja. Lisäksi jos tapahtuma kestää pitkään, SQL-tietokantaan luodaan "haamutietueita". Haamutietueet vaikuttavat kielteisesti järjestelmän kaikkiin prosesseihin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
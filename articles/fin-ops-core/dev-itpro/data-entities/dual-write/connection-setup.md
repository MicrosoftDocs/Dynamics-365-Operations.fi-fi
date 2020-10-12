---
title: Kaksoiskirjoituksen asetusten tuetut skenaariot
description: Tässä ohjeaiheessa kuvataan skenaariot, joita tuetaan kaksoiskirjoituksen asetuksia varten.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818593"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Kaksoiskirjoituksen asetusten tuetut skenaariot

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Voit määrittää kaksoiskirjoitusyhteyden Finance and Operations -ympäristön ja Common Data Service -ympäristön välille.

+ **Finance and Operations -ympäristö** muodostaa **Finance and Operations -sovellusten** (kuten Microsoft Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin ja Dynamics 365 Retailin) taustaympäristön.
+ **Common Data Service -ympäristö** tarjoaa **Dynamics 365:n mallipohjaisille sovelluksille** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation) taustaympäristön.

>[!IMPORTANT]
>Finance and Operationsin Human Resources tukee kaksoiskirjoitusyhteyksiä, mutta Dynamics 365 Human Resources -sovellus ei.

Asennusmekanismi vaihtelee tilauksen ja ympäristön mukaan.

+ Muutamissa Finance and Operations -sovellusten ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa. Jos sinulla on Power Platformin käyttöoikeus, saat uuden Common Data Service -ympäristön, jos vuokraajalla ei ole sellaista.
+ Finance and Operations -sovellusten olemassa olevissa ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Finance and Operations -ympäristössä.

Seuraavia asetusskenaarioita tuetaan:

+ [Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä](#new-new)
+ [Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä](#new-existing)
+ [Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja uusi mallipohjaisen sovelluksen ilmentymä](#new-demo-new)
+ [Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja olemassa oleva mallipohjaisen sovelluksen ilmentymä](#new-demo-existing)
+ [Olemassa oleva Finance and Operations -sovelluksen ilmentymä ja uusi tai olemassa oleva mallipohjaisen sovelluksen ilmentymä](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä

Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa ei ole tietoja) ja Dynamics 365:n uuden mallipohjaisen sovelluksen ilmentymän välille, seuraa kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita. Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:

- Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.
- Valmistellaan uusi, tyhjä mallipohjaisen sovelluksen ilmentymä, johon on asennettu ensisijainen CRM-ratkaisu.
- Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.
- Yksikkökartat otetaan käyttöön reaaliaikaista synkronointia varten.

Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä

Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa ei ole tietoja) ja Dynamics 365:n olemassa olevan mallipohjaisen sovelluksen ilmentymän välille, seuraa kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita. Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:

- Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.
- Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.
- Yksikkökartat otetaan käyttöön reaaliaikaista synkronointia varten.

Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.

Voit synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen seuraavasti.

1. Luo Finance and Operations -sovellukseen uusi yritys.
2. Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.
3. [Käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.

Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja uusi mallipohjaisen sovelluksen ilmentymä

Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa on esittelytietoja) ja Dynamics 365:n uuden mallipohjaisen sovelluksen ilmentymän välille, seuraa aiemmin tässä ohjeaiheessa olevan [Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä](#new-new) -osan ohjeita. Kun yhteyden määritys on valmis, voit synkronoida esittelytiedot mallipohjaisen sovelluksen kanssa noudattamalla seuraavia ohjeita.

1. Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.
2. Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja olemassa oleva mallipohjaisen sovelluksen ilmentymä

Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa on esittelytietoja) ja Dynamics 365:n olemassa olevan mallipohjaisen sovelluksen ilmentymän välille, seuraa aiemmin tässä ohjeaiheessa olevan [Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä](#new-existing) -osan ohjeita. Kun yhteyden määritys on valmis, voit synkronoida esittelytiedot mallipohjaisen sovelluksen kanssa noudattamalla seuraavia ohjeita.

1. Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.
2. Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.

Voit synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen seuraavasti.

1. Luo Finance and Operations -sovellukseen uusi yritys.
2. Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.
3. [Käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.

Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Olemassa oleva Finance and Operations -sovelluksen ilmentymä ja uusi tai olemassa oleva mallipohjaisen sovelluksen ilmentymä

Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen olemassa olevan ilmentymän ja Dynamics 365:n uuden tai olemassa olevan mallipohjaisen sovelluksen ilmentymän välille Finance and Operation -ympäristössä.

1. Määritä yhteys Finance and Operations -sovelluksesta.
2. Jos haluat synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen, [käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO-yrityskoodia.

Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.

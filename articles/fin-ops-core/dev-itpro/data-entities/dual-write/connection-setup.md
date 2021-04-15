---
title: Kaksoiskirjoituksen määrittämisen ohjeet
description: Tässä ohjeaiheessa kuvataan skenaariot, joita tuetaan kaksoiskirjoituksen asetuksia varten.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 999b37970be1c10fd5e78c3d8ac6c1fb25cad367
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751383"
---
# <a name="guidance-for-dual-write-setup"></a>Kaksoiskirjoituksen määrittämisen ohjeet

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Voit määrittää kaksoiskirjoitusyhteyden Finance and Operations -ympäristön ja Dataverse -ympäristön välille.

+ **Finance and Operations -ympäristö** tarjoaa **Finance and Operations -sovelluksille** (esimerkiksi Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Human Resources) taustaympäristön.
+ **Dataverse-ympäristö** on **asiakkaiden aktivointisovellusten** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation) pohjaympäristö.

> [!IMPORTANT]
> Dynamics 365 Financen Human Resources -moduuli tukee kaksoiskirjoitusyhteyksiä, mutta Dynamics 365 Human Resources -sovellus ei.

Asennusmekanismi vaihtelee tilauksen ja ympäristön mukaan:

+ Muutamissa Finance and Operations -sovellusten ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa. Jos sinulla on Microsoft Power Platformin käyttöoikeus, saat uuden Dataverse -ympäristön, jos vuokraajalla ei ole sellaista.
+ Finance and Operations -sovellusten olemassa olevissa ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Finance and Operations -ympäristössä.

Ennen kaksoiskirjoituksen aloittamista entiteetissä voidaan tehdä ensimmäinen synkronointi, joka käsittelee Finance and Operations -sovellusten ja asiakkaan osallistamissovellusten kummankin puolen aiemmin luodut tiedot. Voit ohittaa ensimmäisen synkronoinnin, jos tietoja ei tarvitse synkronoida ympäristöjen välillä.

Ensimmäisessä synkronoinnissa aiemmin luodut tiedot voivaan kopioida sovelluksesta toiseen kaksisuuntaisesti. Määritysskenaarioita on useita, ja ne määräytyvät käytössä jo olevien ympäristöjen ja niissä olevien tietotyyppien perusteella.

Seuraavia asetusskenaarioita tuetaan:

+ [Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä](#new-new)
+ [Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä](#new-existing)
+ [Uusi Finance and Operations -sovelluksen esiintymä, jolla on tietoja, ja uusi asiakkaan osallistamissovelluksen esiintymä](#new-data-new)
+ [Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä](#new-data-existing)
+ [Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä](#existing-new)
+ [Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymä (jossa ei ole tietoja) ja asiakkaan osallistamissovelluksen esiintymän välille, noudata kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita. Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:

- Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.
- Valmistellaan uusi, tyhjä asiakkaan osallistamissovelluksen esiintymä, johon on asennettu ensisijainen CRM-ratkaisu.
- Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.
- Taulukartat otetaan käyttöön reaaliaikaista synkronointia varten.

Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän (jossa ei ole tietoja) ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille, noudata kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita. Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:

- Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.
- Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.
- Taulukartat otetaan käyttöön reaaliaikaista synkronointia varten.

Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.

Voit synkronoida olemassa olevat Dataverse -tiedot Finance and Operations -sovellukseen seuraavasti.

1. Luo Finance and Operations -sovellukseen uusi yritys.
2. Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.
3. [Käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.
4. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on jäljempänä tässä aiheessa olevassa [Esimerkissä](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja uusi asiakkaan osallistamissovelluksen esiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän ja asiakkaan osallistamissovelluksen uuden esiintymän välille, seuraa ohjeita, jotka tämän ohjeaiheen osassa [Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamissovelluksen esiintymä](#new-new). Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.

1. Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän ja asiakkaan aiemmin luodun osallistamissovelluksen esiintymän välille, noudata ohjeita, jotka ovat tämän ohjeaiheen osassa [Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä](#new-existing). Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.

1. Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Voit synkronoida olemassa olevat Dataverse -tiedot Finance and Operations -sovellukseen seuraavasti.

1. Luo Finance and Operations -sovellukseen uusi yritys.
2. Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.
3. [Käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.
4. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä

Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen aiemmin luodun esiintymän ja asiakkaan osallistamissovelluksen uuden esiintymän välille Finance and Operation -ympäristössä.

1. [Yhteyden määrittäminen Finance and Operations -sovelluksessa](enable-dual-write.md).
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä

Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen aiemmin luodun esiintymän ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille Finance and Operation -ympäristössä.

1. [Yhteyden määrittäminen Finance and Operations -sovelluksessa](enable-dual-write.md).
2. Jos haluat synkronoida olemassa olevat Dataverse -tiedot Finance and Operations -sovellukseen, [käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO-yrityskoodia.
3. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="example"></a>Esimerkki

Esimerkkiin voi tutustua kohdassa [Asiakkaiden V3 ottaminen käyttöön – yhteyshenkilöiden taulun yhdistämismääritys](enable-entity-map.md#enable-table-map)

Lisätietoja vaihtoehtoisesta tavasta, joka perustuu kunkin entiteetin tietomääriin, kun niissä on suoritettava ensimmäinen synkronointi, on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
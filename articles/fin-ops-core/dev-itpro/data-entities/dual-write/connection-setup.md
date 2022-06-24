---
title: Kaksoiskirjoituksen määrittämisen ohjeet
description: Tässä artikkelissa kuvataan skenaariot, joita tuetaan kaksoiskirjoituksen asetuksia varten.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a0d1b4e1f093874a8fd37cf7aadb331cd1e7adc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873146"
---
# <a name="guidance-for-dual-write-setup"></a>Kaksoiskirjoituksen määrittämisen ohjeet

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Voit määrittää kaksoiskirjoitusyhteyden taloushallinnon ja toimintojen ympäristön ja Dataverse-ympäristön välille.

+ **Taloushallinnon ja toimintojen ympäristö** muodostaa **talous- ja toimintosovellusten** (kuten Microsoft Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin, Dynamics 365 Commercen ja Dynamics 365 Human Resourcesin) taustaympäristön.
+ **Dataverse-ympäristö** on **asiakkaiden aktivointisovellusten** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation) pohjaympäristö.

> [!IMPORTANT]
> Dynamics 365 Financen Human Resources -moduuli tukee kaksoiskirjoitusyhteyksiä, mutta Dynamics 365 Human Resources -sovellus ei.

Asennusmekanismi vaihtelee tilauksen ja ympäristön mukaan:

+ Muutamissa taloushallinnon ja toimintojen sovellusten ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa. Jos sinulla on Microsoft Power Platformin käyttöoikeus, saat uuden Dataverse -ympäristön, jos vuokraajalla ei ole sellaista.
+ Muutamissa aiemmin luoduissa taloushallinnon ja toimintojen sovellusten ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa taloushallinnon ja toimintojen ympäristössä.

Ennen kaksoiskirjoituksen aloittamista entiteetissä voidaan tehdä ensimmäinen synkronointi, joka käsittelee taloushallinnon ja toimintojen sovellusten ja asiakkaan osallistamissovellusten kummankin puolen aiemmin luodut tiedot. Voit ohittaa ensimmäisen synkronoinnin, jos tietoja ei tarvitse synkronoida ympäristöjen välillä.

Ensimmäisessä synkronoinnissa aiemmin luodut tiedot voivaan kopioida sovelluksesta toiseen kaksisuuntaisesti. Määritysskenaarioita on useita, ja ne määräytyvät käytössä jo olevien ympäristöjen ja niissä olevien tietotyyppien perusteella.

Seuraavia asetusskenaarioita tuetaan:

+ [Uusi taloushallinnon ja toimintojen sovelluksen esiintymä ja uusi asiakkaan osallistamissovelluksen esiintymä](#new-new)
+ [Uusi taloushallinnon ja toimintojen sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä](#new-existing)
+ [Uusi taloushallinnon ja toimintojen sovelluksen esiintymä, jossa on tietoja, ja uusi asiakkaan osallistamissovelluksen esiintymä](#new-data-new)
+ [Uusi taloushallinnon ja toimintojen sovelluksen esiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä](#new-data-existing)
+ [Aiemmin luotu taloushallinnon ja toimintojen sovelluksen esiintymä ja uusi asiakkaan osallistamissovelluksen esiintymä](#existing-new)
+ [Aiemmin luotu taloushallinnon ja toimintojen sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Uusi taloushallinnon ja toimintojen sovelluksen esiintymä ja uusi asiakkaan osallistamissovelluksen esiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden taloushallinnon ja toimintojen sovelluksen uuden esiintymä (jossa ei ole tietoja) ja asiakkaan osallistamissovelluksen esiintymän välille, noudata kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita. Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:

- Uusi, tyhjä taloushallinnon ja toimintojen ympäristö valmistellaan.
- Valmistellaan uusi, tyhjä asiakkaan osallistamissovelluksen esiintymä, johon on asennettu ensisijainen CRM-ratkaisu.
- Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.
- Taulukartat otetaan käyttöön reaaliaikaista synkronointia varten.

Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Uusi taloushallinnon ja toimintojen sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden taloushallinnon ja toimintojen sovelluksen uuden esiintymän (jossa ei ole tietoja) ja aiemmin luodun asiakkaan osallistamissovelluksen esiintymän välille, noudata kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita. Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:

- Uusi, tyhjä taloushallinnon ja toimintojen ympäristö valmistellaan.
- Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.
- Taulukartat otetaan käyttöön reaaliaikaista synkronointia varten.

Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.

Voit synkronoida olemassa olevat Dataverse-tiedot taloushallinnon ja toimintojen sovellukseen seuraavasti.

1. Luo uusi yritys taloushallinnon ja toimintojen sovelluksessa.
2. Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.
3. [Käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.
4. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on jäljempänä tässä artikkelissa olevassa [Esimerkki](#example)-osassa.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Uusi taloushallinnon ja toimintojen sovelluksen esiintymä, jossa on tietoja, ja uusi asiakkaan osallistamissovelluksen esiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden talous- ja toimintosovellusten uuden esiintymän (jossa on tietoja) ja asiakkaan osallistamissovelluksen uuden esiintymän välille, seuraa ohjeita, jotka ovat tämän artikkelin [Uusi talous- ja toimintosovellusten esiintymä ja uusi asiakkaan osallistamissovelluksen esiintymä](#new-new) -osassa. Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.

1. Avaa taloushallinnon ja toimintojen sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Uusi taloushallinnon ja toimintojen sovelluksen esiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden talous- ja toimintosovellusten uudenesiintymän (jossa on tietoja) ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille, seuraa ohjeita, jotka ovat tämän artikkelin [Uusi talous- ja toimintosovellusten esiintymä ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä](#new-existing) -osassa. Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.

1. Avaa taloushallinnon ja toimintojen sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Voit synkronoida olemassa olevat Dataverse-tiedot taloushallinnon ja toimintojen sovellukseen seuraavasti.

1. Luo uusi yritys taloushallinnon ja toimintojen sovelluksessa.
2. Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.
3. [Käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.
4. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Aiemmin luotu taloushallinnon ja toimintojen sovelluksen esiintymä ja uusi asiakkaan osallistamissovelluksen esiintymä

Kaksoiskirjoitusyhteyden määrittäminen aiemmin luodun sovelluksen aiemmin luodun esiintymän ja asiakkaan osallistamissovelluksen uuden esiintymän välille taloushallinnon ja toimintojen ympäristössä.

1. [Määritä yhteys taloushallinnon ja toimintojen sovelluksesta ](enable-dual-write.md).
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Aiemmin luotu taloushallinnon ja toimintojen sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä

Kaksoiskirjoitusyhteyden määrittäminen aiemmin luodun sovelluksen aiemmin luodun esiintymän ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille taloushallinnon ja toimintojen ympäristössä.

1. [Määritä yhteys taloushallinnon ja toimintojen sovelluksesta ](enable-dual-write.md).
2. Jos haluat synkronoida olemassa olevat Dataverse-tiedot taloushallinnon ja toimintojen sovellukseen, [käynnistä](bootstrap-company-data.md) Dataverse-tiedot käyttämällä kolmen kirjaimen ISO-yrityskoodia.
3. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="example"></a>Esimerkki

Esimerkkiin voi tutustua kohdassa [Asiakkaiden V3 ottaminen käyttöön – yhteyshenkilöiden taulun yhdistämismääritys](enable-entity-map.md#enable-table-map)

Lisätietoja vaihtoehtoisesta tavasta, joka perustuu kunkin entiteetin tietomääriin, kun niissä on suoritettava ensimmäinen synkronointi, on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
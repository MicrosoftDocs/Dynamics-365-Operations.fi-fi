---
title: Kaksoiskirjoituksen määrittämisen ohjeet
description: Tässä artikkelissa kuvataan skenaariot, joita tuetaan kaksoiskirjoituksen asetuksia varten.
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 15dfb609b5e25b4faf2b913cc2310df71c88a74d
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111246"
---
# <a name="guidance-for-dual-write-setup"></a>Kaksoiskirjoituksen määrittämisen ohjeet

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Voit määrittää kaksoiskirjoitusyhteyden talous- ja toimintosovellusympäristön sekä Dataverse-ympäristön välille.

+ **Talous- ja toimintosovellusympäristö** muodostaa **talous- ja toimintosovellusten** (kuten Microsoft Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin, Dynamics 365 Commercen ja Dynamics 365 Human Resourcesin) taustaympäristön.
+ **Dataverse-ympäristö** on **asiakkaiden aktivointisovellusten** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation) pohjaympäristö.


> [!IMPORTANT]
> Dynamics 365 Financen Human Resources -moduuli tukee kaksoiskirjoitusyhteyksiä, mutta Dynamics 365 Human Resources -sovellus ei.

Asennusmekanismi vaihtelee tilauksen ja ympäristön mukaan:

+ Uusissa talous- ja toimintosovellusten esiintymissä kaksoiskirjoitusyhteyden määrittäminen alkaa Microsoft Dynamics Lifecycle Servicesissä (LCS). Jos sinulla on Microsoft Power Platformin käyttöoikeus, saat uuden Dataverse -ympäristön, jos vuokraajalla ei ole sellaista.
+ Aiemmin luoduissa talous- ja toimintosovellusten esiintymissä kaksoiskirjoitusyhteyden määrittäminen alkaa talous- ja toimintosovellusympäristössä.

Ennen kaksoiskirjoituksen aloittamista entiteetissä voidaan tehdä ensimmäinen synkronointi, joka käsittelee talous- ja toimintosovellusten sekä asiakkaan osallistamissovellusten kummankin puolen aiemmin luodut tiedot. Voit ohittaa ensimmäisen synkronoinnin, jos tietoja ei tarvitse synkronoida ympäristöjen välillä.

Ensimmäisessä synkronoinnissa aiemmin luodut tiedot voivaan kopioida sovelluksesta toiseen kaksisuuntaisesti. Määritysskenaarioita on useita, ja ne määräytyvät käytössä jo olevien ympäristöjen ja niissä olevien tietotyyppien perusteella.

Seuraavia asetusskenaarioita tuetaan:

+ [Uusi talous- ja toimintosovellusesiintymä sekä uusi asiakkaan osallistamissovellusesiintymä](#new-new)
+ [Uusi talous- ja toimintosovellusesiintymä sekä aiemmin luotu asiakkaan osallistamissovellusesiintymä](#new-existing)
+ [Uusi talous- ja toimintosovellusesiintymä, jossa on tietoja, sekä uusi asiakkaan osallistamissovellusesiintymä](#new-data-new)
+ [Uusi talous- ja toimintosovellusesiintymä, jossa on tietoja, sekä aiemmin luotu asiakkaan osallistamissovellusesiintymä](#new-data-existing)
+ [Aiemmin luotu talous- ja toimintosovellusesiintymä sekä uusi asiakkaan osallistamissovellusesiintymä](#existing-new)
+ [Aiemmin luotu talous- ja toimintosovellusesiintymä sekä aiemmin luotu asiakkaan osallistamissovellusesiintymä](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Uusi talous- ja toimintosovellusesiintymä sekä uusi asiakkaan osallistamissovellusesiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden uuden talous- ja toimintosovellusesiintymän (jossa ei ole tietoja) ja asiakkaan osallistamissovellusesiintymän välille, lisätietoja on kohdassa [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md). Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:

- Uusi, tyhjä talous- ja toimintosovellusympäristö valmistellaan.
- Valmistellaan uusi, tyhjä asiakkaan osallistamissovelluksen esiintymä, johon on asennettu ensisijainen CRM-ratkaisu.
- Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.
- Taulukartat otetaan käyttöön reaaliaikaista synkronointia varten.

Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Uusi talous- ja toimintosovellusesiintymä ja aiemmin luotu asiakkaan osallistamissovellusesiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden uuden talous- ja toimintosovellusesiintymän (jossa ei ole tietoja) ja aiemmin luodun asiakkaan osallistamissovellusesiintymän välille, lisätietoja on kohdassa [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md). Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:

- Uusi, tyhjä talous- ja toimintosovellusympäristö valmistellaan.
- Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.
- Taulukartat otetaan käyttöön reaaliaikaista synkronointia varten.

Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.

Voit synkronoida olemassa olevat Dataverse-tiedot talous- ja toimintosovellukseen seuraavasti.

1. Luo uusi yritys talous- ja toimintosovelluksessa.
2. Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.
3. [Käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.
4. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on jäljempänä tässä artikkelissa olevassa [Esimerkki](#example)-osassa.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Uusi talous- ja toimintosovellusesiintymä, jossa on tietoja, ja uusi asiakkaan osallistamissovellusesiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden talous- ja toimintosovellusten uuden esiintymän (jossa on tietoja) ja asiakkaan osallistamissovelluksen uuden esiintymän välille, noudata ohjeita, jotka ovat tämän artikkelin [Uusi talous- ja toimintosovellusesiintymä sekä uusi asiakkaan osallistamissovellusesiintymä](#new-new) -osassa. Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.

1. Avaa talous- ja toimintosovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Uusi talous- ja toimintosovellusesiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovellusesiintymä

Jos haluat määrittää kaksoiskirjoitusyhteyden uuden talous- ja toimintosovellusesiintymän (jossa on tietoja) ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille, seuraa ohjeita, jotka ovat tämän artikkelin [Uusi talous- ja toimintosovellusesiintymä sekä aiemmin luotu asiakkaan osallistamissovellusesiintymä](#new-existing) -osassa. Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.

1. Avaa talous- ja toimintosovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Voit synkronoida olemassa olevat Dataverse-tiedot talous- ja toimintosovellukseen seuraavasti.

1. Luo uusi yritys talous- ja toimintosovelluksessa.
2. Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.
3. [Käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.
4. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Aiemmin luotu talous- ja toimintosovellusesiintymä sekä uusi asiakkaan osallistamissovellusesiintymä

Kaksoiskirjoitusyhteyden määrittäminen aiemmin luodun talous- ja toimintosovellusesiintymän sekä uuden asiakkaan osallistamissovellusesiintymän välille talous- ja toimintosovellusympäristössä.

1. [Määritä yhteys talous- ja toimintosovelluksesta ](enable-dual-write.md).
2. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Aiemmin luotu talous- ja toimintosovellusesiintymä sekä aiemmin luotu asiakkaan osallistamissovellusesiintymä

Kaksoiskirjoitusyhteyden määrittäminen aiemmin luodun talous- ja toimintosovellusesiintymän sekä asiakkaan aiemmin luodun osallistamissovellusesiintymän välille talous- ja toimintosovellusympäristössä.

1. [Määritä yhteys talous- ja toimintosovelluksesta ](enable-dual-write.md).
2. Jos haluat synkronoida aiemmin luodut Dataverse-tiedot talous- ja toimintosovellukseen, [käynnistä](bootstrap-company-data.md) Dataverse-tiedot käyttämällä kolmen kirjaimen ISO-yrityskoodia.
3. Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.

Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).

## <a name="example"></a>Esimerkki

Esimerkkiin voi tutustua kohdassa [Asiakkaiden V3 ottaminen käyttöön – yhteyshenkilöiden taulun yhdistämismääritys](enable-entity-map.md#enable-table-map)

Lisätietoja vaihtoehtoisesta tavasta, joka perustuu kunkin entiteetin tietomääriin, kun niissä on suoritettava ensimmäinen synkronointi, on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

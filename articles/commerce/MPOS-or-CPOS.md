---
title: Modern POS:n (MPOS) tai Cloud POS:n valitseminen
description: Tässä ohjeaiheessa kerrotaan Modern POS:n ja Cloud POS:n tärkeimmät erot. Ohjeaiheessa kerrotaan myös eri tekijöistä, jotka Dynamics 365 Commercein käyttöönottavien jälleenmyyjien tulee ottaa huomioon, kun he määrittävät vaatimuksiaan.
author: jblucher
manager: AnnBe
ms.date: 10/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1fffc7141c041873f39f716aaf1a775984ef499c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022335"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a>Modern POS:n (MPOS) tai Cloud POS:n valitseminen

[!include [banner](includes/banner.md)]

Tämä ohjeaihe sisältää käyttöönoton suorittajille tarkoitettuja lisätietoja taustasta sekä vihjeitä ja ohjeita seikoista, jotka tulee ottaa huomioon ennen Dynamics 365 Commercein käyttöönottoa. Käyttöönoton suorittajat voivat välttää käyttäjien tyytyväisyyteen tai suorituskykyyn liittyviä ongelmia tutustumalla ja seuraamalla näitä ohjeita käyttöönottoprosessin osana.

## <a name="insights"></a>Tietoja

Commerce sisältää laajat käyttöönotto- ja topologiavaihtoehdot. Tämän vuoksi jälleenmyyjät voivat valita liiketoiminnan ja teknologian vaatimuksiin parhaiten sopivat komponentit ja konfiguraation. Myyntipisteen komponentin ympäristön ja lomakekertoimen valinta edellyttää huolellista harkintaa.

### <a name="pos-platform-and-form-factor-considerations"></a>Myyntipisteen ympäristön ja lomakekertoimen huomioon otettavia seikkoja

Commerce tukee seuraavia myyntipisteen vaihtoehtoja:

- Modern POS (MPOS) Microsoft Windowsille
- Microsoft Windows Phonen MPOS
- Apple iPad- tai Google Android -tabletin MPOS
- Microsoft Edge-, Internet Explorer- ja Google Chrome -selaimia tukeva Cloud POS (CPOS)

Kaikissa tapauksissa myyntipiste (MPOS ja CPOS) jakaa saman ydinsovelluksen koodin. Tämä on tärkeää seuraavista syistä:

- Käyttöliittymän on yhdenmukainen ympäristöstä tai lomakekertoimesta riippumatta.
- Useimmat toiminnalliset kapasiteetit ovat samat ympäristöstä ja lomakekertoimesta riippumatta. Niillä on kuitenkin tärkeitä eroavaisuuksiakin. Niistä kerrotaan tässä ohjeaiheessa.
- Myyntipisteiden vaihtelut voidaan yhdistää ja suorittaa samanaikaisesti tietyssä myymälässä. Esimerkiksi pääkassakoneissa jälleenmyyjä voi käyttää MPOS:ia Windows-käyttöjärjestelmän tietokoneissa. Jälleenmyyjä voi kuitenkin täydentää kassakoneita selainpohjaisilla päätteillä tai mobiililaitteilla.
- Ympäristöissä ja lomakekertoimissa voidaan tehdä helposti mukautuksia ja laajennuksia. Koska ydinsovelluksen koodi on jaettu, useimmat mukautukset voidaan ottaa käyttöön vain kerran useiden kertojen sijaan.

### <a name="mpos-vs-cpos"></a>MPOS vs. CPOS

Vaikka MPOS ja CPOS ovat pääosin samanlaisia, niissä on joitakin tärkeitä eroja, jotka on tärkeä tietää.

#### <a name="mpos"></a>MPOS

Windows-, iOS- tai Android-laitteessa käytettävä MPOS on sovellus, joka on pakattu ja asennettu kyseiseen laitteeseen ja jota ylläpidetään laitteessa.

- **Windows** – Windows-sovelluksen MPOS sisältää kaiken sovelluskoodin ja upotetun Commerce Runtime (CRT) -ympäristön. 
- **iOS/Android** – Näissä ympäristöissä sovellus toimii CPOS-sovelluskoodin isäntänä. Toisin sanoen sovelluskoodi saadaan CPOS-palvelimesta Microsoft Azuressa tai Commerce Scale Unit -yksiköstä. Lisätietoja on kohdassa [Retail Store Scale Unit -vähittäismyyntilaitteen yleiskatsaus](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

Koska CPOS suoritetaan selaimessa, sovellusta ei asenneta laitteeseen. Sen sijaan selain käyttää sovelluskoodia CPOS-palvelimesta. Tämän vuoksi CPOS ei voi käyttää myyntipisteen laitteistoa suoraan tai käsitellä tietoja offline-tilassa.

### <a name="store-deployment-considerations"></a>Myymälän käyttöönotossa huomioon otettavia seikkoja

Ympäristön ja lomakekertoimen lisäksi jälleenmyyjien on valittava myymälälle myös käyttöönottovaihtoehto. Seuraavassa taulukossa esitetään jokaisen myyntipistevaihtoehdon käytettävissä olevat konfiguraatiot.

| Myyntipisteen sovellus         | Commerce Scale Unit | Käytettävissä offline-tilassa |
|-------------------------|---------------|-------------------|
| Windowsin MPOS        | Pilvi tai RSSU | Kyllä               |
| iOS:n tai Androidin MPOS | Pilvi tai RSSU | Ei                |
| Cloud POS               | Pilvi tai RSSU | Ei                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit on komponentti, joka isännöi CRT-kenttää. CRT sisältää kaiken myyntipisteen käyttämän liiketoimintalogiikan sekä mahdollistaa kanavatietokannan käytön. Myymälän kaikki myyntipisteen asiakkaat voivat käyttää Commerce Scale Unit -palvelinta online-tilassa. Commerce Scale Unit voidaan ottaa käyttöön joko pilvessä tai myymälässä.

#### <a name="offline-mode"></a>Offline-tila

Windowsin MPOS tukee offline-tilaa. Myyntipiste voi jatkaa myynnin käsittelemistä offline-tilassa, vaikka se ei olisi enää yhteydessä Commerce Scale Unit -palvelimeen. Myyntipiste voidaan synkronoida kanavatietokannan kanssa, kun yhteys on jälleen muodostettu. MPOS käyttää omaa upotettua CRT-esiintymää ja väliaikaisesti sen omaa paikallista tietolähdettä (SQL Server -offline-tietokanta). Lisätietoja offline-toiminnoista on kohdassa [Myyntipisteen offline-toiminnot](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality).

### <a name="pos-peripheralhardware-considerations"></a>Myyntipisteen oheislaitteen/laitteiston huomioon otettavia seikkoja

Jälleenmyyjien on myös pohdittava, miten myyntipiste käyttää oheislaitteita, kuten tulostimia, kassoja ja maksupäätteitä. Vain Windowsin MPOS tukee suoraa viestintää näiden laitteiden kanssa. Windows Phonen, iOS:n, tai Androidin MPOS ja Cloud POS vaativat laiteaseman, jotta näihin laitteisiin voi muodostaa yhteyden. Laiteasemat voidaan varata myyntipisteen kassakoneelle tai ne voidaan jakaa myymälän kassakoneiden kesken. Lisätietoja laiteasemista kohdassa [Retail-laiteaseman määrittäminen ja asentaminen](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Toteutuksessa huomioitavaa

Ota seuraavat tiedot huomioon, kun suunnittelet myyntipisteen käyttöönottoa myymälöissä:

- **Toiminnalliset vaatimukset** – Liiketoiminnan perusprosessit ja -kapasiteetit ovat samat ympäristöstä, lomakekertoimesta ja käyttöönoton topologiasta riippumatta. Tämän vuoksi suurimman osan jälleenmyyjistä ei tarvitse miettiä toiminnallisia vaatimuksia käyttöönoton suunnittelun yhteydessä.
- **Yhteydet** – Verkon saatavuus (suuralueverkko \[WAN\] ja lähiverkko \[LAN\]) on tärkein tekijä, joka vaatii huolellista harkintaa. Järjestelmän on oltava liiketoiminnan kannalta tärkeiden prosessien käytettävissä. Jos näin ei ole, tilasäästöjen ja pilvipalveluratkaisun tuomien kustannussäästöjen ja käytön yksinkertaisuuuden edut menetetään.

    Jos annetun laitteen yhteys on hyvin luotettava ja vikasietoinen tai jos jälleenmyyjä hyväksyy tietyn käyttämättömyysajan, suosittelemme jompaakumpaa seuraavista vaihtoehdoista:

    - Käytä MPOS:ia Windows ja ota offline-tila käyttöön.
    - Ota käyttöön paikallinen Commerce Scale Unit.

    Nämä kaksi vaihtoehtoa eivät sulje toisiaan pois. Jälleenmyyjät saavat luotettavimman topologian ottamalla käyttöön paikallisen RSSU. Se vähentää riippuvuutta Internet-yhteydestä tai Azuren käytettävyydestä. Sen avulla voidaan myös ottaa käyttöön myyntipisteen kassakoneita, joissa on käytössä offline-tila, jos paikallisessa palvelimessa tai verkossa on ongelmia.

- **Laitteiston laitteet/oheislaitteet** – Eräs tärkeä Retail POS -järjestelmän näkökulma on myyntipisteiden oheislaitteiden, kuten tulostimien, kassojen ja maksupäätteiden, käyttäminen. Vaikka kaikissa käytettävissä olevissa myyntipisteiden vaihtoehdoissa voidaan käyttää oheislaitteita, vain Windowsin MPOS tukee niitä suoraan. Kaikki muut sovellukset vaativat vähintään yhden laiteaseman. Vaikka tämä lähestymistapa lisää joustavuutta, lisäkomponentit on otettava käyttöön, määritettävä ja ylläpidettävä.
- **Järjestelmävaatimukset** – Myyntipistesovellusten järjestelmävaatimukset vaihtelevat. Muista tarkistaa uusimmat tiedot, ennen kuin teet valinnan. Koska esimerkiksi CPOS suoritetaan selaimessa, se tukee useampia käyttöjärjestelmiä. Lisätietoja järjestelmävaatimuksista on kohdassa [Pilvikäyttöönottojen järjestelmävaatimukset](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Käyttöönotto ja ylläpito** – Käyttöönoton ja ylläpidon monimutkaisuus voi vaihdella sovelluksen ja käyttöönottovalintojen mukaan. Esimerkiksi pilvipalvelun CPOS-käyttöönotossa asennusta ja päivitystä ei tarvitse tehdä jokaiseen laitteeseen. Siksi tämä vaihtoehto on huomattavasti yksikertaisempi ja halvempi. Jos otat käyttöön MPOS:n jokaisessa kassakoneessa ja otat käyttöön offline-tilan sekä jaetut laiteasemat, hallinnoitavien päätepisteiden lukumäärä on huomattavasti isompi.

---
title: Valitse Store Commerce tai Cloud POS
description: Tässä artikkelissa kerrotaan Store Commerce- ja Cloud POS -myyntipisteen väliset erot ja kuvataan useita tekijöitä, joiden avulla Dynamics 365 Commercen käyttöön ottavat vähittäismyyjät voivat valita parhaan vaihtoehdon tarpeidensa mukaan.
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: bbb5f3d4c61907243bed404f3ab7bea05c78b1c0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276451"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Valitse Store Commerce tai Cloud POS

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan Store Commerce- ja Cloud POS -myyntipisteen väliset erot ja kuvataan useita tekijöitä, joiden avulla Dynamics 365 Commercen käyttöön ottavat vähittäismyyjät voivat valita parhaan vaihtoehdon tarpeidensa mukaan. Tämä ohjeaihe sisältää käyttöönoton suorittajille tarkoitettuja lisätietoja taustasta sekä vihjeitä ja ohjeita seikoista, jotka tulee ottaa huomioon ennen Dynamics 365 Commercen käyttöönottoa. Käyttöönoton suorittajat voivat välttää käyttäjien tyytyväisyyteen tai suorituskykyyn liittyviä ongelmia tutustumalla ja seuraamalla näitä ohjeita käyttöönottoprosessin osana.

## <a name="insights"></a>Tietoja

Commerce sisältää laajat käyttöönotto- ja topologiavaihtoehdot. Tämän vuoksi jälleenmyyjät voivat valita liiketoiminnan ja teknologian vaatimuksiin parhaiten sopivat komponentit ja konfiguraation. Myyntipisteen komponentin ympäristön ja lomakekertoimen valinta edellyttää huolellista harkintaa.

### <a name="pos-platform-and-form-factor-considerations"></a>Myyntipisteen ympäristön ja lomakekertoimen huomioon otettavia seikkoja

Commerce tukee seuraavia myyntipisteen vaihtoehtoja:

- Store Commerce Microsoft Windowsille
- Store Commerce iOS- ja Android-ympäristöihin
- Microsoft Edge- ja Google Chrome -selaimia tukeva Cloud POS (CPOS)
- Modern POS (MPOS) Microsoft Windowsille (MPOS vanhenee lokakuussa 2023.) 

Kaikissa tapauksissa myyntipisteet (Store Commerce ja CPOS) jakavat saman ydinsovelluksen koodin. Tämä on tärkeää seuraavista syistä:

- Käyttöliittymän on yhdenmukainen ympäristöstä tai lomakekertoimesta riippumatta.
- Useimmat toiminnalliset kapasiteetit ovat samat ympäristöstä ja lomakekertoimesta riippumatta. Niillä on kuitenkin tärkeitä eroavaisuuksiakin. Niistä kerrotaan tässä artikkelissa.
- Myyntipisteiden vaihtelut voidaan yhdistää ja suorittaa samanaikaisesti kussakin myymälässä. Esimerkiksi pääkassakoneissa jälleenmyyjä voi käyttää Store Commercea Windows-käyttöjärjestelmän tietokoneissa. Jälleenmyyjä voi kuitenkin täydentää kassakoneita selainpohjaisilla päätteillä tai mobiililaitteilla.
- Ympäristöissä ja lomakekertoimissa voidaan tehdä helposti mukautuksia ja laajennuksia. Koska ydinsovelluksen koodi on jaettu, useimmat mukautukset voidaan ottaa käyttöön vain kerran useiden kertojen sijaan.

### <a name="store-commerce-vs-cpos"></a>Store Commerce vs. CPOS

Vaikka Store Commerce ja CPOS ovat pääosin samanlaisia, niissä on joitakin tärkeitä eroja, jotka on tärkeä tietää.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce on työpöytäsovellus, joka asennetaan ja huolletaan laitteella.

- **Windows** – Windows-sovelluksen Store Commerce sisältää kaiken sovelluskoodin ja upotetun Commerce Runtime (CRT) -ympäristön ja Hardware Station (HWS) -laitteistoaseman.
- **iOS/Android** – Näissä ympäristöissä sovellus toimii CPOS-sovelluskoodin isäntänä. Toisin sanoen sovelluskoodi saadaan CPOS-palvelimesta, jota ylläpidetään Commerce Scale Unitissa. Lisätietoja on kohdassa [Commerce Store Scale Unit -yleiskatsaus](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Koska CPOS suoritetaan selaimessa, sovellusta ei asenneta laitteeseen. Sen sijaan selain käyttää sovelluskoodia CPOS-palvelimesta. Tämän vuoksi CPOS ei voi käyttää myyntipisteen laitteistoa suoraan tai käsitellä tietoja offline-tilassa.

### <a name="store-deployment-considerations"></a>Myymälän käyttöönotossa huomioon otettavia seikkoja

Ympäristön ja lomakekertoimen lisäksi jälleenmyyjien on valittava myymälälle myös käyttöönottovaihtoehto. Seuraavassa taulukossa esitetään jokaisen myyntipistevaihtoehdon käytettävissä olevat konfiguraatiot.

| Myyntipisteen sovellus            | Commerce Scale Unit | Käytettävissä offline-tilassa | Paikallinen HWS-tuki |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce Windowsille | Pilvi tai RSSU       | Kyllä               | Kyllä               |
| Store Commerce Androidille | Pilvi tai RSSU       | En                | Kyllä               |
| Store Commerce iOS-ympäristöön     | Pilvi tai RSSU       | En                | En                |
| Cloud POS                  | Pilvi tai RSSU       | En                | En                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit on komponentti, joka isännöi CRT-kenttää. CRT sisältää kaiken myyntipisteen käyttämän liiketoimintalogiikan sekä mahdollistaa kanavatietokannan käytön. Myymälän kaikki myyntipisteen asiakkaat voivat käyttää Commerce Scale Unit -palvelinta online-tilassa. Commerce Scale Unit voidaan ottaa käyttöön joko pilvessä tai myymälässä.

#### <a name="offline-mode"></a>Offline-tila

Store Commerce Windowsille tukee offline-tilaa. Myyntipiste voi jatkaa myynnin käsittelemistä offline-tilassa, vaikka se ei olisi enää yhteydessä Commerce Scale Unit -palvelimeen. Myyntipiste voidaan synkronoida kanavatietokannan kanssa, kun yhteys on jälleen muodostettu. Store Commerce käyttää omaa upotettua CRT-esiintymää ja väliaikaisesti sen omaa paikallista tietolähdettä (SQL Server -offline-tietokanta). Lisätietoja offline-toiminnoista on kohdassa [Myyntipisteen offline-toiminnot](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>Myyntipisteen oheislaitteen/laitteiston huomioon otettavia seikkoja

Jälleenmyyjien on myös pohdittava, miten myyntipiste käyttää oheislaitteita, kuten tulostimia, kassoja ja maksupäätteitä. Laiteasemat voidaan varata myyntipisteen kassakoneelle tai ne voidaan jakaa myymälän kassakoneiden kesken.

| Myyntipisteen sovellus            | Paikallinen HWS OPOS | Verkon oheislaitteet | Jaettu HWS-tuki |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce Windowsille | Kyllä            | Kyllä                 | Kyllä                |
| Store Commerce Androidille | En             | Kyllä                 | Kyllä                |
| Store Commerce iOS-ympäristöön     | En             | En                  | Kyllä                |
| Cloud POS                  | En             | En                  | Kyllä                |

Lisätietoja laiteasemista kohdassa [Retail-laiteaseman määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Toteutuksessa huomioitavaa

Ota seuraavat tiedot huomioon, kun suunnittelet myyntipisteen käyttöönottoa myymälöissä:

- **Toiminnalliset vaatimukset** – Liiketoiminnan perusprosessit ja -kapasiteetit ovat samat ympäristöstä, lomakekertoimesta ja käyttöönoton topologiasta riippumatta. Tämän vuoksi suurimman osan jälleenmyyjistä ei tarvitse miettiä toiminnallisia vaatimuksia käyttöönoton suunnittelun yhteydessä.
- **Yhteydet** – Verkon saatavuus (suuralueverkko \[WAN\] ja lähiverkko \[LAN\]) on tärkein tekijä, joka vaatii huolellista harkintaa. Järjestelmän on oltava liiketoiminnan kannalta tärkeiden prosessien käytettävissä. Jos näin ei ole, tilasäästöjen ja pilvipalveluratkaisun tuomien kustannussäästöjen ja käytön yksinkertaisuuuden edut menetetään.

    Jos annetun laitteen yhteys on hyvin luotettava ja vikasietoinen tai jos jälleenmyyjä hyväksyy tietyn käyttämättömyysajan, suosittelemme jompaakumpaa seuraavista vaihtoehdoista:

    - Käytä Store Commercea Windowsissa ja ota offline-tila käyttöön.
    - Ota käyttöön paikallinen Commerce Scale Unit.

    Nämä kaksi vaihtoehtoa eivät sulje toisiaan pois. Jälleenmyyjät saavat luotettavimman topologian ottamalla käyttöön paikallisen RSSU. Se vähentää riippuvuutta Internet-yhteydestä tai Azuren käytettävyydestä. Sen avulla voidaan myös ottaa käyttöön myyntipisteen kassakoneita, joissa on käytössä offline-tila, jos paikallisessa palvelimessa tai verkossa on ongelmia.

- **Laitteiston laitteet/oheislaitteet** – Eräs tärkeä Retail POS -järjestelmän näkökulma on myyntipisteiden oheislaitteiden, kuten tulostimien, kassojen ja maksupäätteiden, käyttäminen. Vaikka kaikissa käytettävissä olevissa myyntipisteiden vaihtoehdoissa voidaan käyttää oheislaitteita, vain Windowsin Store Commerce tukee niitä suoraan. Kaikki muut sovellukset vaativat vähintään yhden laiteaseman. Vaikka tämä lähestymistapa lisää joustavuutta, lisäkomponentit on otettava käyttöön, määritettävä ja ylläpidettävä.
- **Järjestelmävaatimukset** – Myyntipistesovellusten järjestelmävaatimukset vaihtelevat. Muista tarkistaa uusimmat tiedot, ennen kuin teet valinnan. Koska esimerkiksi CPOS suoritetaan selaimessa, se tukee useampia käyttöjärjestelmiä. Lisätietoja järjestelmävaatimuksista on kohdassa [Pilvikäyttöönottojen järjestelmävaatimukset](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Käyttöönotto ja ylläpito** – Käyttöönoton ja ylläpidon monimutkaisuus voi vaihdella sovelluksen ja käyttöönottovalintojen mukaan. Esimerkiksi pilvipalvelun CPOS-käyttöönotossa asennusta ja päivitystä ei tarvitse tehdä jokaiseen laitteeseen. Siksi tämä vaihtoehto on huomattavasti yksikertaisempi ja halvempi. Jos otat käyttöön Store Commercen jokaisessa kassakoneessa ja otat käyttöön offline-tilan sekä jaetut laiteasemat, hallinnoitavien päätepisteiden lukumäärä on huomattavasti isompi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Kaksoiskirjoituksen asetukset Lifecycle Servicesistä
description: Tässä artikkelissa käsitellään kaksoiskirjoitusyhteyden määrittämistä Microsoft Dynamics Lifecycle Servicesistä (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: laswenka
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: dda0b20492a109e4c3781db520ac19c325e0b403
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289175"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Kaksoiskirjoituksen asetukset Lifecycle Servicesistä

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa käsitellään kaksoiskirjoitusyhteyden käyttöön ottamista Microsoft Dynamics Lifecycle Servicesistä (LCS).

## <a name="prerequisites"></a>Edellytykset

Asiakkaiden on suoritettava Power Platform -integrointi seuraavien ohjeaiheiden mukaan:

- Jos et vielä käytä Microsoft Power Platformia ja haluat laajentaa talous- ja toimintosovellusten ympäristöjä lisäämällä ominaisuuksia, katso [Power Platform -integrointi - Ota käyttöön ympäristön käyttöönoton aikana](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Jos sinulla jo on Dataverse- ja Power Platform -ympäristöt ja yhdistää ne talous- ja toimintosovellusten ympäristöihin, katso [Power Platform -integrointi – Ota käyttöön ympäristön käyttöönoton jälkeen](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Määritä kaksoiskirjoitus uusille tai olemassa oleville Dataverse-ympäristöille

Noudattamalla näitä ohjeita voit määrittää kaksoiskirjoituksen LCS-**ympäristön tiedot** -sivulla:

1. Laajenna **Power Platform -integrointi** -osa **Ympäristön tiedot** -sivulla.

2. Valitse **Kaksoiskirjoitussovellus**-näppäin.

    ![Power Platform -integrointi.](media/powerplat_integration_step2.png)

3. Lue ehdot ja valitse valintaruutu ja valitse sitten **Määritä**.

4. Jatka valitsemalla **OK**.

5. Voit seurata etenemistä päivittämällä säännöllisesti ympäristön tietosivun. Asetusten määritys kestää yleensä 30 minuuttia tai vähemmän.  

6. Kun asetukset on tehty, näyttöön tulee sanoma, jossa näkyy, onko prosessi onnistunut tai onko siinä ollut virhe. Jos asennus epäonnistui, näyttöön tulee liittyvä virhesanoma. Virheet on korjattava ennen seuraavaan vaiheeseen siirtymistä.

7. Luo linkki Dataversen ja nykyisen ympäristön tietokantojen välille valitsemalla **Yhdistä Power Platform -ympäristöön**. Tämä kestää yleensä alle 5 minuuttia.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Yhdistä Power Platform -ympäristöön.":::

8. Kun yhdistäminen on valmis, hyperlinkki tulee näkyviin. Linkin avulla voit kirjautua sisään kaksoiskirjoitusalueelle talous- ja toimintosovellusympäristössä. Siellä voit tehdä entiteettien yhdistämismäärityksiä.

## <a name="linking-mismatch"></a>Linkitysristiriita

On mahdollista, että kaksoiskirjoitusympäristösi on linkitetty Dataverse-esiintymään, kun taas LCS:tä ei ole määritetty Power Platform -integrointia varten. Linkittämisen vastaamattomuus voi aiheuttaa odottamattomia toimintoja. On suositeltavaa, että LCS-ympäristön tiedot vastaavat sitä, mihin olet muodostanut yhteyden kaksoiskirjoituksessa, jotta liiketoimintatapahtumat, virtuaalitaulukot ja lisäosat voivat käyttää samaa yhteyttä.

Jos ympäristössä on linkitysristiriita, LCS näyttää ympäristön tietosivulla seuraavaa esimerkkiä vastaavan varoituksen: "Microsoft on havainnut, että ympäristö on linkitetty kaksoiskirjoituksella muuhun kuin Power Platform -integroinnissa määritettyyn kohteeseen, mikä ei ole suositeltavaa."

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform -integroinnin linkkiristiriita":::

Jos saat tämän varoituksen, kokeile jotakin seuraavista ratkaisuista:

- Jos LCS-ympäristöäsi ei ole koskaan määritetty Power Platform -integrointia varten, voit noudattamalla tämän artikkelin ohjeita muodostaa yhteyden Dataverse-esiintymään, joka on määritetty kaksoiskirjoituksessa.
- Jos LCS-ympäristösi on jo määritetty Power Platform -integrointia varten, sinun tulisi poistaa kaksoiskirjoituksen linkitys ja yhdistää se uudelleen LCS:n määrittämään kohteeseen käyttämällä [skenaariota: linkityksen palauttaminen tai muuttaminen](relink-environments.md#scenario-reset-or-change-linking).

Aiemmin oli käytettävissä manuaalinen tukipalvelupyyntövaihtoehto, mutta se oli ennen kuin yllä kuvattu vaihtoehto 1 oli olemassa.  Microsoft ei enää tue tukipalvelupyynnön kautta lähetettäviä manuaalisia uudelleenlinkittämispyyntöjä.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


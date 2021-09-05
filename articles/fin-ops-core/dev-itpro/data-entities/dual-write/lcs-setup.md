---
title: Kaksoiskirjoituksen asetukset Lifecycle Servicesistä
description: Tässä aiheessa käsitellään kaksoiskirjoitusyhteyden määrittämistä Microsoft Dynamics Lifecycle Servicesistä (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2cfe6d882c5de763164ddb4a344cba2991c88783
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416648"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Kaksoiskirjoituksen asetukset Lifecycle Servicesistä

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä aiheessa käsitellään kaksoiskirjoitusyhteyden käyttöön ottamista Microsoft Dynamics Lifecycle Servicesistä (LCS).

## <a name="prerequisites"></a>Edellytykset

Power Platform -integrointi on suoritettava seuraavien ohjeaiheiden mukaan:

+ [Power Platform -integrointi - Ota käyttöön ympäristön käyttöönoton aikana](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform -integrointi - Määritä ympäristön käyttöönoton jälkeen](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Määritä kaksoiskirjoitus uusille Dataverse-ympäristöille

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

8. Kun yhdistäminen on valmis, hyperlinkki tulee näkyviin. Linkin avulla voit kirjautua sisään kaksoiskirjoitusalueelle Finance and Operations -ympäristössä. Siellä voit tehdä entiteettien yhdistämismäärityksiä.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Määritä kaksoiskirjoitus olemassa olevalle Dataverse-ympäristölle

Määrittääksesi kaksoiskirjoituksen aiemmin luotuun Dataverse-ympäristöön, sinun tulee luoda Microsoft [tukipyyntö](../../lifecycle-services/lcs-support.md). Pyynnössä on oltava seuraavat tiedot:

+ Finance and Operations -ympäristösi tunnus.
+ Lifecycle Services -ympäristösi nimi.
+ Dataverse-organisaatiotunnus tai Power Platform -ympäristötunnus Power Platform -hallintakeskuksesta. Pyydä tukipyynnössäsi, että esiintymän tunnusta voi käyttää Power Platform -integroinnissa.

> [!NOTE]
> Et voi poistaa ympäristöjen välistä linkitystä LCS-sovelluksen avulla. Jos haluat poistaa linkityksen, avaa **Tietojen integrointi** -työtila Finance and Operations -ympäristössä ja valitse sitten **Poista linkitys**.

## <a name="linking-mismatch"></a>Linkitysristiriita

On mahdollista, että LCS-ympäristö on linkitetty yhteen Dataverse-esiintymään samalla, kun kaksoiskirjoitusympäristö on linkitetty toiseen Dataverse-esiintymään. Linkitysristiriita voi aiheuttaa odottamatonta toimintaa, ja tämän seurauksena on mahdollista, että tiedot lähetetään väärään ympäristöön. Kaksoiskirjoituksessa käytettävä suositusympäristö on se, joka luotiin Power Platform -integroinnin osana, ja pitkällä aikavälillä tämä on ainoa tapa muodostaa linkki ympäristöjen välille.

Jos ympäristössä on linkitysristiriita, LCS näyttää ympäristön tietosivulla seuraavankaltaisen varoituksen: Microsoft on havainnut, että ympäristö on linkitetty kaksoiskirjoituksella muuhun kuin Power Platform -integroinnissa määritettyyn kohteeseen, mikä ei ole suositeltavaa.

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform -integroinnin linkkiristiriita":::

Jos tämä virhe esiintyy, valittavissa on tarpeiden mukaan kaksi vaihtoehtoa:

+ [Kaksoiskirjoitusympäristöjen linkityksen poistaminen ja uudelleenlinkittäminen (linkityksen palauttaminen tai muuttaminen)](relink-environments.md#scenario-reset-or-change-linking) LCS-ympäristön tietosivun määrityksen mukaisesti. Tämä on paras vaihtoehto, koska se voidaan suorittaa ilman Microsoftin tukea.  
+ Jos kaksoiskirjoituksen linkki halutaan säilyttää, Microsoftin tukea voidaan pyytää muuttaa Power Platform -integrointi käyttämään aiemmin luotua Dataverse-ympäristöä edellisessä osassa käsitellyllä tavalla.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

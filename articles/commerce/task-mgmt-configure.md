---
title: Tehtävienhallinnan määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten tehtävienhallintatoiminnot määritetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0ae0f3bd58db587d9024beceedd790cc3d3e4ee990a2f4c727dfda96b2f0785c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730800"
---
# <a name="configure-task-management"></a>Tehtävien hallinnan määrittäminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tehtävienhallintatoiminnot määritetään Microsoft Dynamics 365 Commerce -sovelluksessa.

Ennen kuin Dynamics 365 Commercen päälliköt ja työntekijät voivat käyttää tehtävienhallintatoimintoja Commercessa, tehtävienhallinta on määritettävä. Määritysvaiheet sisältävät käyttöoikeuksien myöntämisen päälliköille ja työntekijöille, käyttöoikeuksien jakelun myyntipisteen asiakassovelluksille, myyntipisteen ilmoitusten määrittämisen ja myyntipistesovelluksen aloitussivun **Tehtävät**-ruudun määrittämisen.

## <a name="configure-permissions-for-store-managers"></a>Myymäläpäälliköiden käyttöoikeuksien määrittäminen

Jokainen määritetyn myymälän työntekijä voi tarkastella kaikkia myymälälle määritettyjä tehtäviä. He voivat myös päivittää heille määritettyjen tehtävien tilan. Esimerkiksi myymäläpäälliköillä on oltava tehtävienhallinnan käyttöoikeudet, jotta he voivat hallita myymälälle määritettyjä tehtäviä ja luoda yhden tarkoituksen tehtäviä.

Voit määrittää myymäläpäälliköiden tehtävienhallinnan käyttöoikeudet seuraavien vaiheiden avulla.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Työntekijät \> Käyttöoikeusryhmät**.
1. Valitse tietty käyttöoikeusryhmä (esimerkiksi **Päällikkö**) ja valitse sitten **Muokkaa**.
1. Määritä **Käyttöoikeudet**-pikavälilehdessä **Salli tehtävienhallinta** -asetuksen arvoksi **Kyllä**.
1. Lisää **Ilmoitukset**-pikavälilehdessä **Tehtävienhallinta**-toiminto ja anna arvo **Näyttöjärjestys**-kenttään. Anna esimerkiksi arvo **2**, jos **Tilauksen täyttäminen** -toiminnon **Näyttöjärjestys**-kohdan arvo on jo **1**.
    
> [!NOTE]
> Jos muulla kuin päälliköllä on oltava tehtävienhallinnan käyttöoikeudet myyntipisteessä, voit myöntää tälle henkilölle käyttöoikeudet. Vaihtoehtoisesti voit luoda uuden käyttöoikeusryhmän muille kuin päälliköille ja määrittää **Salli tehtävienhallinta** -asetuksen arvoksi **Kyllä**.

Seuraavassa kuvassa näkyy, miten myymäläpäälliköiden tehtävienhallinnan käyttöoikeudet määritetään.

![Myymäläpäälliköiden tehtävienhallinnan käyttöoikeuksien määrittäminen.](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Työntekijöiden käyttöoikeuksien määrittäminen

Työntekijöillä on oltava oikeus luoda tehtäväluetteloita, hallita määritysehtoja ja määrittää minkä tahansa tehtäväluettelon toistuminen. Jos haluat määrittää nämä käyttöoikeudet, määritä työntekijöille **vähittäismyynnin tehtävienhallinnan** rooli.

Voit määrittää työntekijälle käyttöoikeudet seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Työntekijät \> Käyttäjät**.
1. Valitse työntekijä.
1. Valitse **Käyttäjän roolit** -pikavälilehdessä **Määritä roolit**.
1. Valitse **Määritä roolit käyttäjälle** -valintaikkunassa **vähittäismyynnin tehtävienhallinnan** rooli ja valitse **OK**.

## <a name="distribute-permissions-to-pos-clients"></a>Käyttöoikeuksien jakelu myyntipisteen asiakassovelluksille

Ennen kuin työntekijät voivat käyttää myyntipisteen asiakassovelluksia, niille on jaettava käyttöoikeudet ja käyttöoikeudet on synkronoitava.

Voit jakaa myyntipisteen asiakassovellusten käyttöoikeudet seuraavasti.

1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Valitse **1060** (**Henkilöstö**) -jakeluaikataulu ja valitse sitten **Suorita nyt**.
1. Valitse **1070** (**Kanavan määritys**) -jakeluaikataulu ja valitse sitten **Suorita nyt**.

## <a name="configure-pos-notifications-for-tasks"></a>Myyntipisteen ilmoitusten määrittäminen tehtäville

Tehtävienhallinta on määritettävä niin, että ilmoitukset ovat käytettävissä myyntipistesovelluksessa.

Voit määrittää myyntipisteen ilmoitukset tehtäville seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Myyntipistetoiminnot**.
1. Etsi toiminto **1400** (**Tehtävienhallinta**) ja valitse sen **Ota ilmoitukset käyttöön** -valintaruutu.

Seuraavassa kuvassa on **Tehtävienhallinta**-toiminto **Myyntipistetoiminnot**-sivulla.

![Tehtävienhallintatoiminto Myyntipistetoiminnot-sivulla.](media/HQ-POS-Tasks-Notifications.png)

Lisärtietoja myyntipisteen ilmoitusten määrittämisestä on kohdassa [Tilausilmoitusten näyttäminen myyntipisteessä](notifications-pos.md).

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Tehtävät-ruudun määrittäminen myyntipistesovelluksen aloitussivulla

Ennen kuin voit määrittää **Tehtävät**-ruudun myyntipistesovelluksen aloitussivulla, katso lisätietoja myyntipisteen näytön asettelun uusien painikkeiden määrittämisestä ja lisäämisestä kohdasta [Myyntipisteen näytön asettelut](pos-screen-layouts.md).

Määritä **Tehtävät**-ruutu myyntipistesovelluksen aloitussivulla seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Näytön asettelut**.
1. Valitse näytön asettelu. Valitse asettelun koko ja valitse sitten painikeruudukko.
1. Valitse **Painikeruudukot**-pikavälilehdessä **Suunnittelutoiminto**, jos haluat muokata valittua painikeruudukkoa.
1. Lisää **Tehtävät**-ruutu aloitussivun soveltuvaan osaan.

Seuraavassa kuvassa on esimerkki **Tehtävät**-ruudusta myyntipisteen aloitussivulla.

![Myyntipisteen aloitussivun Tehtävät-ruutu.](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tehtävien hallinnan yleiskatsaus](task-mgmt-overview.md)

[Tehtäväluetteloiden luominen ja tehtävien lisääminen](task-mgmt-create-lists.md)

[Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille](task-mgmt-assign-lists.md)

[Tehtävien hallinta myyntipisteessä](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Veromääritysten mukauttaminen perustietojen hakuun
description: Tässä ohjeaiheessa selitetään, miten veromäärityksiä mukautetaan päätietojen hakutoiminnon laajentamista varten.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 498201d5c0377058e86b25953ebbe401ae1af9e3
ms.sourcegitcommit: ed43ceae9b2ef3f616b81127bcf4c4b0862e23f5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2021
ms.locfileid: "7714877"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Veromääritysten mukauttaminen perustietojen hakuun

[!include [banner](../includes/banner.md)]

Tämän aiheen ohjeita noudattamalla voit mukauttaa veromäärityksiä päätietojen hakutoiminnon laajentamista varten.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Microsoftin tarjoaman veromäärityksen tuominen

1. Valitse Regulatory Configuration Servicen (RCS) **Sähköinen raportointi**-työtilassa **Microsoft**-määrityslähde.
2. Valitse **Säilöt**.
3. Valitse **Yleinen** ja valitse sitten **Avaa**.
4. Valitse veromääritys, kuten **Veronlaskennan määritys** ja valitse sitten versio **Versiot**-välilehdestä.
5. Valitse **Tuo**.

> [!NOTE]
> Oletusarvoisesti tuodaan Dataversen mallimääritys. Jos näyttöön tulee varoitussanomia määrityksen tuontiprosessin aikana, ota virtuaaliyksiköt käyttöön Dataversessä. Lisätietoja: [Dataversen virtuaaliyksikköjen käyttöönotto](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Mukautetun tietomallin määrityksen luominen

1. Valitse **Sähköinen raportointi** -työtilassa **Veromääritykset** ja valitse sitten laajennettava tietomallimääritys. Valitse esimerkiksi **Verolaskennan tietomalli**.
2. Valitse **Luo konfiguraatio**.
3. Valitse **Verotettavan asiakirjan malli, johdettu nimestä: Verotietomalli, Microsoft.**
4. Kirjoita **Nimi**-kenttään **Mukautustietomalli**.
5. Valitse **Luo konfiguraatio**.

## <a name="create-customized-reference-models"></a>Mukautettujen viitemallien luominen

1. Valitse **Veromääritykset**-sivulla **Mukautustietomalli** ja valitse sitten **Suunnitteluohjelma**.
2. Valitse moduulin kolmen pisteen painike (**...**) ja valitse sitten **Viitemalli**-näkymä.

    [![Viitemalli.](./media/pic2.png)](./media/pic2.png)

3. Mukautetun viitemallin luominen. Mukautettu malli on päämalli. Mukautettu yksikkö on tietueluettelo. Mukautettu kenttä on merkkijonokenttä, jota haluat käyttää haussa. Voit lisätä kenttiä tarpeen mukaan.
4. Valitse moduulin kolmen pisteen painike (**...**) ja valitse sitten **Verotettava asiakirja** -näkymä.
5. Valitse mukautettuun viitemalliin sidottava määrite. Valitse esimerkiksi **Mukautettu määrite** ja noudata sitten näitä ohjeita:

    1. Valitse **Valitse viitemalli**.
    2. Valitse **Mukautettu malli** ja valitse sitten **OK**. Viitemallin nimeksi päivitetään **Luonnollinen avain** -kentän arvo.

        [![Valitse viitemallin valintaikkuna.](./media/pic5.png)](./media/pic5.png)

    3. Valitse ensin **Tallenna** ja sitten **Viimeistele**.

## <a name="create-a-customized-model-mapping-configuration"></a>Mukautetun tietomallin yhdistämismäärityksen luominen

1. Valitse **Sähköinen raportointi** -työtilassa **Veromääritykset** ja valitse sitten **Dataverse-mallin määritys** -määritys.
2. Valitse **Mallimäärityksen oletusarvo** -kentässä **Ei**.
3. Valitse **Luo konfiguraatio**.
4. Valitse **Verotettavan asiakirjan mallimääritys, johdettu nimestä: Dataversen mallimääritys, Microsoft**.
5. Kirjoita **Nimi**-kenttään **Mukautustietomallin määritys**.
6. Valitse **Kohdemalli**-kentässä **Mukautustietomalli**-tietomalli.
7. Valitse **Luo konfiguraatio**.

    [![Avattava Luo konfigurointi -luettelo -valintaruutu.](./media/pic6.png)](./media/pic6.png)

8. Vallitse **Mukautusmallin määritys** ja määritä **Yhdistetty sovellus** -kentän arvoksi yhteys, joka luotiin vaiheen 8 kohdassa [Ympäristön määrittäminen päätietojen hakua varten](tax-service-set-up-environment-master-data-lookup.md).
9. Määritä **Mallimäärityksen oletusarvo** -kentän arvoksi **Kyllä**.

## <a name="create-customized-model-mappings"></a>Mukautettujen mallimääritysten luominen

1. Valitse **Veromääritykset**-sivulla **Mukautusmallin määritys**.
2. Valitse **Suunnitteluohjelma** ja valitse sitten **Mukautusmalli**.

    [![Mukautusmalli.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Yhdistä mallimääritys Dataverse-yksikköön

1. Valitse **Mallimäärityksen suunnitteluohjelma**-sivulla **Mukautusmalli** ja valitse sitten **Suunnitteluohjelma**.
2. Valitse **Tietolähdetyypit**-puussa **Dataverse-taulu**.
3. Valitse **Tietolähteet**-välilehdessä **Lisää juuri**.
4. Syötä **Nimi**-kenttään **Mukautettu Dataverse**.
5. Valitse toisessa **Nimi**-kentässä yksikkö.
6. Valitse **OK**.

    [![Taulu-tietolähteen ominaisuuksien valintaikkuna.](./media/pic9.png)](./media/pic9.png)

7. Valitse **Mukautettu Dataverse** ja **Mukautettu yksikkö** ja valitse sitten **Sido**.

    [![Mukautettu Dataverse ja mukautettu yksikön sitominen.](./media/pic10.png)](./media/pic10.png)

8. Valitse **Mukautettu Dataverse** -kohdassa ja **Mukautettu kenttä** -kohdassa kenttä ja valitse sitten **Sido**.

    [![Mukautettu Dataverse ja mukautettu kentän sitominen.](./media/pic11.png)](./media/pic11.png)

9. Valitse ensin **Tallenna** ja sitten **Viimeistele**.

## <a name="create-a-customized-tax-configuration"></a>Mukautetun veromäärityksen luominen

1. Valitse **Sähköinen raportointi** -työtilassa **Veromääritykset** ja valitse sitten **Verolaskennan määritys**.
2. Valitse **Luo konfiguraatio**.
3. Valitse **Veropalvelun määritys, johdettu nimestä Verolaskennan määritys, Microsoft**.
4. Kirjoita **Nimi**-kenttään **Mukautuksen määritys**.
5. Valitse **Luo konfiguraatio**.
6. Valitse **Mukautuksen määritys** ja valitse sitten **Suunnitteluohjelma**.
7. Valitse **Tietomalli**-kentässä **Mukautustietomalli**.
8. Valitse **Tietomallin versio** -kentästä vastaava tietomallin versio.

    [![Ominaisuusosa.](./media/pic13.png)](./media/pic13.png)

9. Valitse **Valmis**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

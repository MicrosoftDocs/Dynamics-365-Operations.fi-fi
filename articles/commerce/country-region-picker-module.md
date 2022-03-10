---
title: Maan tai alueen valitsinmoduuli
description: Tässä ohjeaiheessa käsitellään maan tai alueen valitsinmoduulia ja kuvataan, miten se määritetään Microsoft Dynamics 365 Commercessa.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 1a8eebb589372051272573895a0ae5b4203eef62
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109778"
---
# <a name="countryregion-picker-module"></a>Maan tai alueen valitsinmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään maan tai alueen valitsinmoduulia ja kuvataan, miten se määritetään Microsoft Dynamics 365 Commercessa.

Maan tai alueen valitsinmoduuli käyttää Dynamics 365 Commercen [maantieteellisen sijainnin tunnistuksen ja uudelleenohjauksen](geo-detection-redirection.md) oinaisuutta näyttääkseen suositeltuja URL-osoitteita asiakkaille, jotka pyytävät sellaisen sähköisen kaupankäyntisivuston URL-osoitetta, joka ei liity heidän maahansa tai alueeseensa.

Esimerkiksi Kanadassa oleva asiakas voi pyytää sellaisen sivun URL-osoitetta, joka ei liity Kanadaan. Tällöin maan tai alueen valitsinmoduuli näyttää valintaikkunan, joka suosittelee Kanadaan liittyvien sivustojen URL-osoitteita. Seuraavassa kuvassa on esimerkki maan tai alueen valitsimen valintaikkunasta.

![Esimerkki maan tai alueen valitsimen valintaikkunasta aloitussivulla.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Maan tai alueen valitsinmoduulin ominaisuudet

| Ominaisuuden nimi              | Arvo       | kuvaus |
| -------------------------- | ----------- | ----------- |
| Otsikko                    | Teksti        | Valintaikkunan yläosassa näkyvä otsikko. |
| Alaotsikko                 | Teksti        | Otsikon alapuolella oleva alaotsikko. |
| Maa: Näytön merkkijono    | Teksti        | URL-vaihtoehdon näyttönimi (esim. Kanada). |
| Maa: Näytön alimerkkijono | Teksti        | URL-vaihtoehdon valinnainen näytön alimerkkijono (esim. "englanti" tai "ranska"). |
| Maa: Maakuva     | Mediaresurssi | URL-vaihtoehtoon yhdistetty valinnainen kuva (esim. Kanadan lipun kuva). |
| Maa: Maan URL       | Teksti        | URL-osoite, joka vastaa maalle tai alueelle Commercen sivunluontiohjelman **Kanavat**-sivulla (**Sivuston asetukset \> Kanavat**) määritettyä maata ja sijaintia. URL-osoitteen on vastattava täysin **Kanavat**-sivulla määritettyä URL-osoitetta. |
| Toimintolinkki                | Toimintolinkki | Valinnainen linkki, joka näkyy valintaikkunan alaosassa. Tämä linkki voi viedä esimerkiksi sisäiselle sivulle, joka sisältää luettelon kaikista sivuston tukemista maista ja alueista. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Maan tai alueen valitsinmoduulin lisääminen sivulle

Maan tai alueen valitsinmoduulin voi lisätä otsikkomoduuliin joko suoraan tai yhteisen katkelman avulla. Lisätietoja otsikkomoduuleista: [Otsikkomoduuli](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Maan tai alueen valitsinmoduulin määrittäminen Commercen sivustonluontiohjelmassa

> [!NOTE]
> Asiakkaille suosittelemiasi URL-osoitteet on määritettävä maaobjekteiksi maan tai alueen valitsinmoduulissa.

Noudata Commercen sivustonluontiohjelmassa seuraavia ohjeita kaikkien niiden URL-osoitteiden osalta, jotka haluat näyttää ja antaa suosituksena asiakkaille.

1. Valitse maan tai alueen valitsinmoduulin paikka.
1. Valitse ominaisuusruudun **Maaluettelo**-kohdassa **Lisää maa**.
1. Valitse uusi **Maa**-ikkuna.
1. Anna **Näytön merkkijono** -kentässä näyttönimi (esimerkiksi **Kanada**).
1. Valinnainen: anna **Näytön alimerkkijono** -kentässä näytön alimerkkijono (kuten **ranska** tai **fr-ca**).
1. Valinnainen: Valitse kuva mediakirjastosta.
1. Kirjoita **Maan URL**-kenttään URL-osoite. Tämän URL-osoitteen on oltava täsmälleen sama kuin **Kanavat**-sivulla näkyvän URL-osoitteen ja se yhdistetään kanavaan sisältäen sijainnin, joka on yhdistetty maahan tai alueeseen.
1. Valitse **OK**.
1. Toista nämä vaiheet kaikkien muiden URL-osoitteiden osalta, joiden haluat näkyvän maan tai alueen valitsinmoduulissa.

## <a name="additional-resources"></a>Lisäresurssit

[Maantieteellisen sijainnin tunnistuksen ja uudelleenohjauksen määritys](geo-detection-redirection.md)

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ylätunnistemoduuli](author-header-module.md)

[Sivuston valitsinmoduuli](site-selector.md)

[Navigointipolkumoduuli](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

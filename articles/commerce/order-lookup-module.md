---
title: Tilaushakumoduuli
description: Tässä artikkelissa on tietoja tilaushakumoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commercessä.
author: bicyclingfool
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a891de4a1da6641a02b8316d16ac2e9a8180fac1
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734246"
---
# <a name="order-lookup-module"></a>Tilaushakumoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja tilaushakumoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commercessä.

Tilaushakumoduulissa on lomake, jonka avulla asiakkaat voivat hakea tilauksia, jotka he ovat tehneet sähköisen kaupankäynnin sivustolla. Sitä käytetään osana [Tilaushaun käyttöönotto vierailijoiden uloskuittauksessa](order-lookup-guest.md) -ominaisuutta. Tilaushakumoduulia voi käyttää sellaisten tilausten hakemiseen, jotka on tehty sähköisen kaupankäynnin sivustolla, vähittäismyynnin myyntipisteessä tai puhelinkeskuksessa. Lomakkeella voi noutaa sekä vieraskäyttäjien että rekisteröityneiden käyttäjien tilauksia.

Seuraavassa kuvassa on esimerkki lomakkeesta, jonka tilaushakumoduuli on hahmontanut. Kun asiakkaat täyttävät lomakkeen ja valitsevat **Etsi oma tilaus**, heidät ohjataan tilaustietosivulle.

![Tilaushakumoduulin lomake sivulla.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Tilaushakumoduulin ominaisuudet

| Ominaisuuden nimi     | Arvo     | kuvaus |
|-------------------|-----------|-------------|
| Otsikko           | Teksti      | Lomakkeen yläosassa näkyvä otsikko (esim. Etsi oma tilaus). |
| Muotoiltu teksti         | Muotoiltu teksti | Valinnainen selitysteksti, joka näkyy otsikon alapuolella. |
| Tilauksen tilatyyppi | Valintalista      | <p>Valitse tietotyyppi, jota lomake pyytää asiakkaalta tilausvahvistustunnuksen lisäksi. Tällä hetkellä tuetaan seuraavia arvoja:</p><ul><li><b>Sähköposti</b> – Lomake sisältää kentän, johon asiakkaat voivat syöttää tilausta tehdessään käyttämänsä sähköpostiosoitteen.</li><li><b>Ei mitään</b> – Lomake ei pyydä tilausvahvistustunnuksen lisäksi muita tietoja.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Tilaushakumoduulin lisääminen sivulle

Tilaushakumoduulin voi lisätä mihin tahansa sähköisen kaupankäynnin sivuston sivun tekstiosaan. Jos haluat käyttää tilaushakumoduulia mahdollistaaksesi vierailijoiden uloskuittausten tilaushaun, lisää se sellaiselle sivulle, joka ei edellytä käyttäjän kirjautumista. Voit hakea sivun **Vaatii kirjautumisen?** -asetuksen Commercen sivustonluontiohjelman puunäkymässä valitsemalla **Oletussivu (pakollinen)** -paikan ja katsomalla oikeanpuoleisen ruudun alaosaa.


> [!NOTE]
> Jos haluat ottaa tilausten hakutoiminnon käyttöön, varmista, että **Tarjoukset**-avain on käytössä kohdassa **Käyttöoikeuden konfiguraatio** > **Konfigurointiavaimet**.
>
> ![Tarjousten käyttöoikeusavaimen konfiguraation täytyy olla käytössä](./media/Quotations_License_Key_Configuration.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tilaushaun käyttöönotto vierailijoiden uloskuittauksessa](order-lookup-guest.md)

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

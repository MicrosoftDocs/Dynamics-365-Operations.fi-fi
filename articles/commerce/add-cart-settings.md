---
title: Lisää tuote ostoskoriin -asetusten käyttäminen
description: Tässä artikkelissa kuvataan "Lisää tuote ostoskoriin" -asetukset ja miten käyttää niitä Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 336bea289b22e4f6f98077f915d7d35f2a48682d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866027"
---
# <a name="apply-add-product-to-cart-settings"></a>Lisää tuote ostoskoriin -asetusten käyttäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan **Lisää tuote ostoskoriin** -asetukset ja miten käyttää niitä Microsoft Dynamics 365 Commercessa.

Eri työnkulkuja tuetaan, kun ostoskoriin lisätään tuote sähköisen kaupankäynnin Dynamics 365 Commerce -sivustolla. Sivuston käyttäjä voidaan esimerkiksi siirtää ostoskorin sivulle. Vaihtoehtoisesti käyttäjä saattaa jäädä nykyiselle sivulle, mutta hän saa ilmoituksen, jossa vahvistetaan, että tuote on lisätty ostoskoriin.

**Lisää tuote ostoskoriin** -kenttä on käytettävissä Commerce-sivujen luontiohjelman kohdassa **Asetukset \> Laajennukset** eri työnkulkujen tukemiseksi. Valitse jokin seuraavista asetusvaihtoehdoista vastaavan työnkulun toteuttamiseksi:

- **Siirry ostoskorisivulle** – Kun käyttäjät lisäävät nimikkeen ostoskoriin, heidät siirretään ostoskorisivulle.
- **Näytä ilmoitus** – Kun käyttäjät lisäävät nimikkeen ostoskoriin, he saavat vahvistusilmoituksen ja he voivat jatkaa selaamista tuotetietosivulla (PDP).
- **Näytä pienoiskori** – Kun käyttäjät lisäävät nimikkeen ostoskoriin, pienoiskorin sisältö tulee näkyviin. Käyttäjät voivat tarkistaa kaikki ostoskorissa olevat nimikkeet ja jatkaa kassalle, jos he ovat valmiita.
- **Näytä ilmoitus käyttämällä ilmoitusmoduulia** – Kun käyttäjät lisäävät nimikkeen ostoskoriin, ilmoitusmoduulia käytetään vahvistusilmoituksen näyttämiseen. Jotta tämä asetus toimisi, ilmoitusmoduuli täytyy lisätä sivun ylätunnisteeseen.
- **Älä siirry ostoskorisivulle** – Kun käyttäjät lisäävät nimikkeen ostoskoriin, he pysyvät nykyisellä sivulla.

Seuraavassa kuvassa on esimerkki sivuston luontiohjelman **Lisää tuote ostoskoriin** -asetusvaihtoehdoista.

![Esimerkki Lisää tuote ostoskoriin -asetusvaihtoehdoista sivuston luontiohjelmassa](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - **Lisää tuote ostoskoriin** -sivustoasetukset ovat käytettävissä Dynamics 365 Commerce -version 10.0.11 julkaisusta eteenpäin. Jos olet päivittämässä vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Katso ohjeet appsettings.json-tiedoston päivittämiseen kohdasta [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - **Näytä pienoiskori** -asetusvaihtoehto on käytettävissä Dynamics 365 Commerce -version 10.0.20 julkaisusta eteenpäin. Jos olet päivittämässä vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Katso ohjeet appsettings.json-tiedoston päivittämiseen kohdasta [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Seuraavassa kuvassa on esimerkki "Lisätty ostoskoriin" -vahvistusilmoituksesta Fabrikam-sivustolla.

![Esimerkki "Lisätty ostoskoriin" -vahvistusilmoituksesta Fabrikam-sivustolla](./media/ecommerce-addtocart-notifications.PNG)

Seuraavassa kuvassa on esimerkki "Lisätty ostoskoriin" -vahvistusilmoituksesta Adventure Works -sivustolla.

![Esimerkki "Lisätty ostoskoriin" -vahvistusilmoituksesta Adventure Works -sivustolla](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[Myymälän valitsinmoduuli](store-selector.md)

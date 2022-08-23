---
title: Lisää tuote ostoskoriin -asetusten käyttäminen
description: Tässä artikkelissa kuvataan ""Lisää tuote ostoskoriin"" -asetukset ja miten käyttää niitä Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16644e6746d182cd86a40861c4e30a85a9d3d478
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277024"
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

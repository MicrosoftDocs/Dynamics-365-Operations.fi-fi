---
title: Eräseurannassa olevien nimikkeiden parannettu käsitteleminen
description: Tässä aiheessa kuvataan laskelman kirjausprosessin aikana Microsoft Dynamics 365 Commercessa tehtävän eräseurannassa olevien nimikkeiden käsittelyn parannuksia.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 513b6ca84fa71e851a5a3e4275e0b6572789e1eb
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485780"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Eräseurannassa olevien nimikkeiden parannettu käsitteleminen

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan laskelman kirjausprosessin aikana Microsoft Dynamics 365 Commercessa tehtävän eräseurannassa olevien nimikkeiden käsittelyn parannuksia.

Dynamics 365 Commerce -myyntipisteessä eränumeroita ei voi tallentaa eräseurannassa oleville nimikkeille myynnin aikana. Kun myynti kirjataan Commerce-pääkonttorisovelluksessa asiakastilausten tai laskelman kirjauksen avulla, Commerce kuitenkin odottaa, että tietyissä määrityksissä on sallitut eränumerot eräseurannassa oleville nimikkeille ja että niitä käytetään laskutusprosessin aikana.

Jos tuotteilla on sallitut eränumerot, sekä laskelman kirjauksen asiakastilauksen että myyntitilauksen laskutusprosessi käyttää niitä. Jos tuotteille ei ole käytettävissä kelvollisia eränumeroita, asiakastilauksen laskutusprosessi ei voi tehdä kirjauksia, ja myyntipisteen käyttäjä saa virhesanoman. Laskelman kirjaus siirtyy sitten virhetilaan, vaikka tuotteille olisi otettu käyttöön negatiivinen varasto.

Commerceen tehdyt parannukset varmistavat sen, että negatiivisen varaston ollessa käytössä eräseurannassa oleville nimikkeille asiakastilausten ja myyntitilausten laskutusta laskelman kirjauksen kautta ei estetä nimikkeille, jos varasto on 0 (nolla) tai eränumeroa ei ole saatavilla. Parannettu toiminto käyttää myyntiriveissä oletuserätunnusta, kun eränumerot eivät ole saatavilla.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Määritä asiakastilauksissa käytettävä oletuserätunnus

Voit määrittää asiakastilauksissa käytettävän oletuserätunnuksen seuraavasti.

1. Valitse Commerce-pääkonttorisovelluksessa **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commercen parametrit**.
1. Kirjoita arvo **Tilaus**-pikavälilehden **Asiakastilaukset**-välilehden **Oletuserätunnus**-kenttään.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Määritä oletuserätunnus, jota käytetään myyntitilausten laskutuksessa laskelman kirjauksen kautta

Voit määrittää laskelman kirjauksen kautta tapahtuvassa myyntitilausten laskutuksessa käytettävän oletuserätunnuksen seuraavasti.

1. Valitse Commerce-pääkonttorisovelluksessa **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commercen parametrit**.
1. Kirjoita arvo **Varaston päivitys** -pikavälilehden **Kirjaus**-välilehden **Oletuserätunnus**-kenttään.

> [!NOTE]
> - Oletuserätunnuksen toiminto on käytettävissä vain, kun edistynyt varastonhallinta on käytössä tietyn myymälän varastoa ja nimikkeitä varten. Tulevassa versiossa oletuserätunnuksen toimintoa tuetaan myös skenaarioissa, joissa eristynyt varastonhallinta ei ole käytössä.
> - Parannetun eräseurannassa olevien nimikkeiden käsittelyn tuki laskelman kirjaamisen aikana muissa kuin edistyneen varastonhallinnan skenaarioissa sisältyi Commerce-versioon 10.0.5.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

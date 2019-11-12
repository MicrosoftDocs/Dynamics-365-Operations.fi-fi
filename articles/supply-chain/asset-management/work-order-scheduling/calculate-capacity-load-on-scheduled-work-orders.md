---
title: Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen
description: Tässä ohjeaiheessa selitetään, kuinka voit laskea kapasiteettikuormituksen ajoitetuille työtilauksille käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d7684d1a4f78c95ebc7fd0a88f1c7dc7fead0303
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652100"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen

[!include [banner](../../includes/banner.md)]

 

Voit laskea ajoitettujen työtilausten kapasiteetin kuormituksen, jolloin saat yleiskuvan resurssien työkuormituksesta tietyltä kaudelta. Voit tehdä laskelmia seuraavista resursseista: Kunnossapitotyöntekijät, työntekijäryhmät, työkalut ja resurssit.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Ajoitus** > **Kapasiteetin kuormitus**.

2. Valitse **Laske kapasiteetin kuormitus** -valintaikkunan **Näytä**-kentässä, minkä kuormitustyypin haluat laskea: **Kapasiteetti**, **Varattu** vai **Jäljellä oleva määrä**.

3. Valitse **Kyllä** **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa on nolla.

4. Valitse resurssityypit, joille haluat laskea kapasiteetin kuormituksen, valitsemalla **Kyllä** asiaankuuluvissa vaihtopainikkeissa: **Työntekijä**, **Ylläpitotyöntekijäryhmä**, **Työkalu** ja **Resurssi**.

5. Valitse aloituspäivämäärä laskennalle **Aloituspäivämäärä**-kentästä.

6. Valitse **Välityyppi**-kentästä laskutoimitusten väli: **Päivä**, **Viikko**, **Kuukausi** tai **Vuosineljännes**.

7. Lisää **Jakson frekvenssi** -kenttään, kuinka monta aikaväliä haluat laskea. Jos esimerkiksi olet valinnut aika välityypiksi **Päivä** ja lisäät tähän kenttään numeron "5", aloituspäivämäärästä lasketaan viisi päivää eteenpäin.

8. Aloita laskenta valitsemalla **OK**.

Alla oleva kuva näyttää tuloksen, joka kattaa kolme viikkoa kuormitustyypistä **Varattu**.

![Kuva 1](media/08-work-order-scheduling.png)

[!NOTE]
Jos laskennalle valitaan kuormitustyypit **Kapasiteetti** tai **Jäljellä oleva määrä**, sama tulos tulee näkyviin, jos valitun kauden resursseille ei ole tehty varauksia.

Lisätietoja ylläpitoaikataulurivien kapasiteetin kuormituksen laskemisesta ja ajoittamattomista työtilauksista on kohdassa [Kapasiteetin kuormituksen laskeminen](../capacity-planning/calculate-capacity-load.md).


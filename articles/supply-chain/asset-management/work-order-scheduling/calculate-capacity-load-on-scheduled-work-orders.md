---
title: Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen
description: Tässä artikkelissa selitetään, kuinka voit laskea kapasiteettikuormituksen ajoitetuille työtilauksille käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53b147198f6aa9e0254312e5ea48b9ae616a79a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857950"
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

![Kuva 1.](media/08-work-order-scheduling.png)

[!NOTE]
Jos laskennalle valitaan kuormitustyypit **Kapasiteetti** tai **Jäljellä oleva määrä**, sama tulos tulee näkyviin, jos valitun kauden resursseille ei ole tehty varauksia.

Lisätietoja ylläpitoaikataulurivien kapasiteetin kuormituksen laskemisesta ja ajoittamattomista työtilauksista on kohdassa [Kapasiteetin kuormituksen laskeminen](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
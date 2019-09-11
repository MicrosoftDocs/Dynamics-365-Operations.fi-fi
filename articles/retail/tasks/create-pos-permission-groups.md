---
title: Myyntipisteen käyttöoikeusryhmien luominen
description: Tässä ohjeaiheessa kerrotaan, miten voit luoda myyntipisteen käyttöoikeusryhmän.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914790"
---
# <a name="create-pos-permission-groups"></a>Myyntipisteen käyttöoikeusryhmien luominen

[!include[task guide banner](../includes/task-guide-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit luoda myyntipisteen käyttöoikeusryhmän. Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja. Tämä tehtävä on tarkoitettu vähittäismyynnin toiminnoista vastaavan johtajan roolille.

1. Siirry siirtymisruudussa kohtaan **moduulit > Vähittäismyynti > Työntekijät > käyttöoikeusryhmät.**
2. Valitse **Uusi**.
3. Syötä **Myyntipisteen käyttöoikeusryhmän tunnus** -kenttään arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Näytä aikamerkinnät** -kentässä **Kyllä**. Voit ottaa käyttöön myyntipisteen käyttöoikeusryhmän käyttöoikeuksia tai poistaa niitä käytöstä. Joillekin käyttöoikeuksille voi määrittää arvon, jonka avulla arvioidaan, voiko myyntipisteen käyttäjä suorittaa toiminnon. Tässä tehtävän ohjauksessa otetaan käyttöön joitakin käyttöoikeuksia, jotka voidaan antaa kassalle.  
6. Valitse **Salli tilauksen luominen** -kentässä **Kyllä**.
7. Valitse **Salli tilauksen muokkaaminen** -kentässä **Kyllä**.
8. Valitse **Salli tilauksen noutaminen** -kentässä **Kyllä**.
9. Valitse **Salli salasanan vaihtaminen** -kentässä **Kyllä**.
10. Valitse **Salli piilottava sulkeminen** -kentässä **Kyllä**.
11. Valitse **Tallenna**. Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset vähittäismyyntikanaville. 
12. Siirry kohtaan **Siirtymisruutu > Moduulit > Henkilöstöhallinto > Työt > Työt**.
13. Seuraavaksi liitetään myyntipisteen käyttöoikeusryhmä työhön. Etsi haluamasi tietue luettelosta ja valitse se.
14. Valitse **Muokkaa**.
15. Laajenna **Työn luokittelu** -osa.
16. Syötä tai valitse arvo Myyntipisteen käyttöoikeusryhmä -kentässä. Kaikki tämän työn toimissa olevat työntekijät käyttävät näitä myyntipisteen käyttöoikeusryhmän asetuksia, ellei työntekijöiden myyntipisteen käyttöoikeuksia ole ohitettu toimen tasolla.  
17. Valitse **Tallenna**. Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset vähittäismyyntikanaville.  


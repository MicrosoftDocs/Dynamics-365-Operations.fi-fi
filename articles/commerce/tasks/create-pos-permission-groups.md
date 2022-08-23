---
title: Myyntipisteen käyttöoikeusryhmien luominen
description: Tässä artikkelissa kerrotaan, miten voit luoda myyntipisteen käyttöoikeusryhmän.
author: josaw1
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailPosPermissionGroup, HcmJob
ms.openlocfilehash: 0aa394e5dc6685954c31cdddae7cdc042b80af29
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277957"
---
# <a name="create-pos-permission-groups"></a>Myyntipisteen käyttöoikeusryhmien luominen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten voit luoda myyntipisteen käyttöoikeusryhmän. Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja. Tämä tehtävä on tarkoitettu Commerce-toiminnoista vastaavan johtajan roolille.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Retail ja Commerce > Työntekijät > käyttöoikeusryhmät**.
2. Valitse **Uusi**.
3. Syötä **Myyntipisteen käyttöoikeusryhmän tunnus** -kenttään arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Näytä aikamerkinnät** -kentässä **Kyllä**. Voit ottaa käyttöön myyntipisteen käyttöoikeusryhmän käyttöoikeuksia tai poistaa niitä käytöstä. Joillekin käyttöoikeuksille voi määrittää arvon, jonka avulla arvioidaan, voiko myyntipisteen käyttäjä suorittaa toiminnon. Tässä tehtävän ohjauksessa otetaan käyttöön joitakin käyttöoikeuksia, jotka voidaan antaa kassalle.  
6. Valitse **Salli tilauksen luominen** -kentässä **Kyllä**.
7. Valitse **Salli tilauksen muokkaaminen** -kentässä **Kyllä**.
8. Valitse **Salli tilauksen noutaminen** -kentässä **Kyllä**.
9. Valitse **Salli salasanan vaihtaminen** -kentässä **Kyllä**.
10. Valitse **Salli piilottava sulkeminen** -kentässä **Kyllä**.
11. Valitse **Tallenna**. Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset kaupankäyntikanaville. 
12. Siirry kohtaan **Siirtymisruutu > Moduulit > Henkilöstöhallinto > Työt > Työt**.
13. Seuraavaksi liitetään myyntipisteen käyttöoikeusryhmä työhön. Etsi haluamasi tietue luettelosta ja valitse se.
14. Valitse **Muokkaa**.
15. Laajenna **Työn luokittelu** -osa.
16. Syötä tai valitse arvo Myyntipisteen käyttöoikeusryhmä -kentässä. Kaikki tämän työn toimissa olevat työntekijät käyttävät näitä myyntipisteen käyttöoikeusryhmän asetuksia, ellei työntekijöiden myyntipisteen käyttöoikeuksia ole ohitettu toimen tasolla.  
17. Valitse **Tallenna**. Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset kanaville.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

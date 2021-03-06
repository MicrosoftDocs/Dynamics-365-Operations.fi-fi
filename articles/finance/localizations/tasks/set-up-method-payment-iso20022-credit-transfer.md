---
title: Maksutavan määrittäminen ISO20022-tilisiirtoja varten
description: Näiden ohjeiden avulla voi määrittää toimittajan ISO20022-tilisiirron tai minkä tahansa muun maksutyypin luomaan tiedostoja sähköisen raportoinnin avulla.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 643be31db625d0db12f1df18b9e797013da98ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832469"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Maksutavan määrittäminen ISO20022-tilisiirtoja varten

[!include [banner](../../includes/banner.md)]

Näiden ohjeiden avulla voi määrittää toimittajan ISO20022-tilisiirron tai minkä tahansa muun maksutyypin luomaan tiedostoja sähköisen raportoinnin avulla. 

Viennin muotokonfiguraatiot ja maksutilit on määritettävä ennen tämän tehtävän suorittamista.

Tämän tehtävän luomisessa käytettiin esittelytietojen DEMF-yritystä.

Tämä on kolmas viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.

1. Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Maksutapa-kenttää arvolla SEPA CT.
3. Valitse Muokkaa.
4. Valitse Kausi-kentässä Yhteensä.
5. Valitse Maksutyyppi-kentässä Sähköinen maksu.
6. Laajenna Tiedostomuodot-osa.
7. Valitse Yleinen sähköinen raportointi -kentässä Kyllä.
8. Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.
    * Valitse luettelosta arvo ISO20022 - tilisiirto (DE). Jos luettelo on tyhjä, tuotua ja aktiivista toimittajan maksun viennin muotokonfiguraatiota ei ole.  
9. Valitse Tilityyppi-kentässä Pankki.
10. Syötä Maksutili-kenttään arvot DEMF OPER.
11. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
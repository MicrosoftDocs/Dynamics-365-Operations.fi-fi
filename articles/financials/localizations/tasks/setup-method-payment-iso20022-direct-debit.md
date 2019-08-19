---
title: Maksutavan määrittäminen ISO20022-suoraveloitusta varten
description: Näiden ohjeiden avulla voi määrittää asiakkaan ISO20022-suoraveloituksen tai minkä tahansa muun maksutyypin sähköisen raportoinnin avulla.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3c6d8157803e0a8d33520a0cd64fb725e8c9a3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848644"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Maksutavan määrittäminen ISO20022-suoraveloitusta varten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Näiden ohjeiden avulla voi määrittää asiakkaan ISO20022-suoraveloituksen tai minkä tahansa muun maksutyypin sähköisen raportoinnin avulla. 



Viennin muotokonfiguraatiot ja maksutilit on määritettävä ennen tämän tehtävän suorittamista.



Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.



Tämä on kolmas viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.

1. Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksutavat.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Maksutapa-kenttää arvolla ELECTRONIC.
3. Valitse Muokkaa.
4. Syötä Maksutili-kenttään arvot DEMF OPER.
5. Laajenna Tiedostomuodot-osa.
6. Valitse Yleinen sähköinen raportointi -kentässä Kyllä.
7. Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.
    * Valitse luettelosta arvo ISO20022 Direct debit (DE).  Jos luettelo on tyhjä, tuotua ja aktiivista asiakkaan maksun viennin muotokonfiguraatiota ei ole.  
8. Valitse Vaadi valtakirjaa -kentässä Kyllä.
    * Valitse Vaadi valtakirjaa -parametri asiakkaan maksumuodoille, joissa vaaditaan valtakirjatiedot maksuviestissä, kuten SEPA-suoraveloitus.  
9. Valitse Tallenna.


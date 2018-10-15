--- 
title: "Maksutavan määrittäminen ISO20022-suoraveloitusta varten"
description: "Näiden ohjeiden avulla voi määrittää asiakkaan ISO20022-suoraveloituksen tai minkä tahansa muun maksutyypin sähköisen raportoinnin avulla."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 953a3cffc356ab44163944318e7e7d542a113112
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

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



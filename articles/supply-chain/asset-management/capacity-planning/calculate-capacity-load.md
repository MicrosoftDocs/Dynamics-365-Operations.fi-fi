---
title: Laske kapasiteetin kuormitus
description: Tässä ohjeaiheessa kerrotaan, kuinka kapasiteettikuormitus lasketaan resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba4b9ef43e27f689e1f10d2ee8f10f6ea4bf43ed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821726"
---
# <a name="calculate-capacity-load"></a>Laske kapasiteetin kuormitus

[!include [banner](../../includes/banner.md)]


Resurssien hallinnassa voit laskea kapasiteetin kuormituksen:

- ylläpitoaikataulun riveille  
- työtilauksille, joita ei ole vielä ajoitettu  
- ajoitetuille työtilauksille.

Tästä on hyötyä, jos haluat saada yleiskuvan tietyn kauden odotetusta kapasiteetin kuormituksesta. Kapasiteetin kuormituksen laskeminen voidaan tehdä kaikille käyttöomaisuuksille tai valituille käyttöomaisuuksille. Voit myös tehdä laskelmia kunnossapitoseisokkien tai työtilauspoolien osalta.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Kapasiteetin kuormitus** tai **Resurssien hallinta** > **Yhteiset** > **Työtilauspoolit** > **Kaikki työtilauspoolit** / **Aktiiviset työtilauspoolit** > valitse työtilauspooli listasta > **Kapasiteetin kuormitus** -painike tai **Resurssien hallinta** > **Yhteiset** > **Ylläpidon käyttökatkojen toiminnot** > **Kaikki ylläpidon käyttökatkojen toiminnot** / **Aktiiviset ylläpidon käyttökatkojen toiminnot** > valitse ylläpidon toiminno listasta> **Kapasiteetin kuormitus** -painike.

2. Valitse **Laske kapasiteetin kuormitus** -valintaikkunassa laskennan kausi **Alkamispäivämäärä/-kellonaika**- ja **Päättymispäivämäärä/-kellonaika** -kentissä.

3. Valitse **Sisällytä ylläpitoaikataulu** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää ylläpitoaikataulurivit laskelmiin.

4. Valitse **Sisällytä työtilaus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää työttilauksen työt laskelmiin.

5. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kapasiteetin kuormitusriveistä haluat liittyen toiminnallisiin sijainteihin. 

    Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitoaikataulun rivit ja työtilaukset näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. 
    
    Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kunnossapitoaikataulurivit ja kaikki työtilaukset kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

6. Aloita laskenta valitsemalla **OK**.

7. Valitse **Ryhmittely...**-ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Alla olevassa näyttökuvassa valitut **Ryhmittele...**-painikkeet on korostettu sinisellä. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

    ![Kuva 1](media/01-capacity-planning.png)

>[!NOTE]
>Jos haluat keskittyä vain ajoitettujen työtilausten kapasiteettisuunnitteluun, lisätietoja on kohdassa [Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: "Osaston luonti ja sen liittäminen osastohierarkiaan"
description: "Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta. Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta. Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin. Osastot voivat olla tulosvastuullisia."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee51abe108b3bc0aabc764b991222db6d185e532
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a>Osaston luonti ja sen liittäminen osastohierarkiaan

[!include[banner](includes/banner.md)]


Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta. Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta. Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin. Osastot voivat olla tulosvastuullisia.

Osasto voi sisältää kustannuspaikkaryhmän. Osastoille voidaan määrittää toimia. Luo osasto valitsemalla **Henkilöstöhallinto** &gt; **Osastot** &gt; **Osasto**. Seuraavassa taulukossa näkyvät valittavina olevat kentät.

| Kenttä               | Kuvaus                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nimi                | Kirjoita osaston nimi.                                                                                                                                                                                  |
| Osaston numero   | Oletusarvo voidaan luoda automaattisesti, jos numerosarjakoodi on määritetty **Organisaatiotunnus**-viitteeseen **Numerojärjestykset**-sivulla.                                                 |
| Hakunimi         | Kirjoita lyhyt nimi tai lyhenne, jota voidaan käyttää osaston haussa.                                                                                                                                            |
| Muistio                | Anna mahdolliset lisätiedot tässä.                                                                                                                                                                            |
| Hierarkiassa        | Valittuna oleva valintaruutu ilmaisee, että osasto on mukana osastohierarkiassa. Jos haluat tietoja siitä, miten osasto lisätään osastohierarkiaan, ks. tässä artikkelissa myöhemmin annettavat tiedot. |
| DUNS-numero         | DUNS on lyhenne englanninkielisistä sanoista Data Universal Number System. Tämä on yhdeksännumeroinen luku, jonka myöntää Dun & Bradstreet.                                                                                                     |
| Esimies             | Valitse henkilö, joka johtaa osastoa.                                                                                                                                                                    |
| Osoitteet           | Lisää osaston osoitetiedot. Lisää esimerkiksi postitusosoite rakennukselle, jossa osasto sijaitsee.                                                                          |
| Yhteystiedot | Lisää osaston yhteystiedot. Lisää esimerkiksi osaston palvelupisteen puhelinnumero.                                                                                           |

Voit lisätä osaston osastohierarkiaan seuraavasti:

1.  Valitse **Henkilöstöhallinto** &gt; **Osastot** &gt; **Osastohierarkia**.
2.  Valitse **Muokkaa**, ja valitse sitten organisaatio, jonka alle osasto kuuluu.
3.  Napsauta **Lisää**, ja valitse luettelosta **Osasto**.
4.  Valitse näkyviin tulevasta luettelosta hierarkiaan lisättävä osasto.
5.  Tallenna muutokset. Saat sanoman, että hierarkiasta on luotu luonnosversio.
6.  Kun olet valmis, valitse **Julkaise** hierarkian suunnittelutoiminnossa. Voit syöttää voimassaolopäivämäärän, joka ilmaisee, milloin hierarkia tulisi julkaista. Jos esimerkiksi haluat lisätä uuden osaston seuraavan vuoden alusta, aseta voimaantulopäiväksi 1.1. seuraavana kalenterivuonna. Hierarkian muutokset tulevat voimaan tuona päivänä.






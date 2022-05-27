---
title: Osastojen luominen ja sisällyttäminen osastohierarkiaan
description: Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta. Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: cdc0440c02d0e66eaa89bfd875d8c8edf8d99c96
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688598"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Osastojen luominen ja sisällyttäminen osastohierarkiaan


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta. Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta. Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin. Osastot voivat olla tulosvastuullisia.

Osasto voi sisältää kustannuspaikkaryhmän. Osastoille voidaan määrittää toimia. Luo osasto valitsemalla **Henkilöstöhallinto** &gt; **Osastot** &gt; **Osasto**. Seuraavassa taulukossa näkyvät valittavina olevat kentät.

| Kenttä               | Kuvaus                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nimi**                | Kirjoita osaston nimi.                                                                                                                                                                                  |
| **Osaston numero**   | Oletusarvo voidaan luoda automaattisesti, jos numerosarjakoodi on määritetty **Organisaatiotunnus**-viitteeseen **Numerojärjestykset**-sivulla.                                                 |
| **Hakunimi**         | Kirjoita lyhyt nimi tai lyhenne, jota voidaan käyttää osaston haussa.                                                                                                                                            |
| **Muistio**                | Anna mahdolliset lisätiedot tässä.                                                                                                                                                                            |
| **Hierarkiassa**        | Valittuna oleva valintaruutu ilmaisee, että osasto on mukana osastohierarkiassa. Jos haluat tietoja siitä, miten osasto lisätään osastohierarkiaan, ks. tässä artikkelissa myöhemmin annettavat tiedot. |
| **DUNS-numero**         | DUNS on lyhenne englanninkielisistä sanoista Data Universal Number System. Tämä on yhdeksännumeroinen luku, jonka myöntää Dun & Bradstreet.                                                                                                     |
| **Esimies**             | Valitse henkilö, joka johtaa osastoa.                                                                                                                                                                    |
| **Osoitteet**           | Lisää osaston osoitetiedot. Lisää esimerkiksi postitusosoite rakennukselle, jossa osasto sijaitsee.                                                                          |
| **Yhteystiedot** | Lisää osaston yhteystiedot. Lisää esimerkiksi osaston palvelupisteen puhelinnumero.                                                                                           |

Voit lisätä osaston osastohierarkiaan seuraavasti:

1.  Valitse **Henkilöstöhallinto** &gt; **Osastot** &gt; **Osastohierarkia**.
2.  Valitse **Muokkaa**, ja valitse sitten organisaatio, jonka alle osasto kuuluu.
3.  Napsauta **Lisää**, ja valitse luettelosta **Osasto**.
4.  Valitse näkyviin tulevasta luettelosta hierarkiaan lisättävä osasto.
5.  Tallenna muutokset. Saat sanoman, että hierarkiasta on luotu luonnosversio.
6.  Kun olet valmis, valitse **Julkaise** hierarkian suunnittelutoiminnossa. Voit syöttää voimassaolopäivämäärän, joka ilmaisee, milloin hierarkia tulisi julkaista. Jos esimerkiksi haluat lisätä uuden osaston seuraavan vuoden alusta, aseta voimaantulopäiväksi 1.1. seuraavana kalenterivuonna. Hierarkian muutokset tulevat voimaan tuona päivänä.

## <a name="steps-for-creating-a-department"></a>Osaston luontiohjeet
Uuden osaston luomisen vaiheittaiset ohjeet löytyvät [Uusien osastojen määrittäminen](./hr-personnel-define-departments.md) -artikkelissa. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

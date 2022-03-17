---
title: Etuusilmoitus
description: Etuusilmoitus käsittelee etuja, joihin työntekijä on tällä hetkellä rekisteröitynyt.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 602e4f9459aac8fdbea5f2752e51cc2c1b71360c
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358240"
---
# <a name="benefit-statement"></a>Etuusilmoitus


[!INCLUDE [PEAP](../includes/peap-2.md)]

**Etuusilmoitus** on raportti, ja se sisältää etuudet, joihin työntekijä on tällä hetkellä rekisteröitynyt. Työntekijä voi käyttää raporttia suoraan, ja se on myös etujen ylläpitäjän käytettävissä. **Etuusilmoitus** sisältää luettelon eduista, joihin työntekijä on rekisteröitynyt, kattavuusasetukset, kustannukset sekä mahdolliset huollettavat tai edunsaajat. Ilmoitus voidaan tulostaa yhdelle työntekijälle tai useille työntekijöille.

> [!NOTE]
**Etuusilmoitus**-ominaisuus on otettava käyttöön **Ominaisuuksien hallinta** -työtilassa. Sitä varten **Etujen hallinta** on otettava käyttöön ominaisuuksien hallinnassa. 


## <a name="importing-the-benefit-statement"></a>Etuusilmoituksen tuominen 

**Etuusilmoitus** on tuotava raporttimääritysten avulla, ennen kuin **Etuusilmoitus** on käytettävissä. Toimi seuraavasti:

1.  Valitse **Järjestelmän hallinta** -työtila.

2.  Valitse **Sähköinen raportointi** -ruutu.

3.  Valitse ensin **Konfiguraation lähteet** ja sitten **Säilöt**.

  ![Säilöjen valinta](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Valitse luettelossa **HR-resurssit** ja valitse sitten **Avaa**.

    ![Määrityssäilöt](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Valitse vasemmassa ruudussa **Etuusilmoitusmalli** ja laajenna se siten, että **Etuusilmoituksen muoto** näkyy.

6.  Valitse **Etuusilmoituksen muoto** vasemmassa ruudussa.

7.  Näytön oikealla puolella on **Versiot**-pikavälilehti Valitse **Tuo**.

    ![Versiot-pikavälilehti](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Etuusilmoituksen muodostaminen PDF-tiedostona

**Etuusilmoitus** tulostetaan oletusarvoisesti Microsoft Word -asiakirjana. PDF-muodossa tulostamista varten PDF-asetus on määritettävä **Sähköisen raportoinnin kohde** -kohdassa. 

1. Se tehdään valitsemalla **Järjestelmänhallinnan työtila** > **Sähköinen raportointi** > **Liittyvät linkit** > **Sähköisen raportoinnin kohde**.

1.  Valitse **Uusi**.

2.  Valitse **Viite**-kentässä **Etuusilmoituksen muoto**.

3.  Valitse **Tiedostokohde**-pikavälilehdessä **Uusi**.

4.  Kirjoita **Nimi**-kenttään **Etuusilmoitus PDF**.

5.  Valitse **Tiedosto-osan nimi** -kentässä **Etuusilmoitus**.

6.  Valitse **Muunna PDF-tiedostoksi** -valintaruutu.

7.  Valitse valikkokohteessa **Asetukset**. 

    ![Tiedostokohde](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Valitse ensin **Tiedosto**-pikavälilehti ja sitten **Käytössä**.

9.  Valitse **OK**.
   
> [!NOTE]
> Etujen hallintaominaisuus on esiversiotilassa. **Sähköisen raportoinnin kohde** -raportin sähköpostin kohdeasetuksessa on tunnettu ongelma. On mahdollista, että virhesanoma avautuu eikä sähköpostia lähetä.

**Etuusilmoitus** voidaan luoda seuraavilta sivuilta:

-   **Etujen hallinnan työtila** > **Linkit** > **Raportit** > **Etuusilmoitus**

-   **Työntekijät (vanha lomake)** > **Henkilökohtaiset tiedot -välilehti** > **Etuusilmoitus**

-   **Yksinkertaistettu työntekijöiden lisääminen** > **Eturaportit** > **Etuusilmoitus**

-   **Työntekijöiden itsepalvelu** > **Edut** > **Näytä etuusilmoitus**

> [!NOTE]
>  **Etuusilmoituksen** käyttöä **työntekijän itsepalvelussa** hallitaan **Näytä etuusilmoitus** -oikeuden perusteella. Se sijaitsee **Työntekijän itsepalvelun edut** -kohdassa. Tämä oikeus annetaan työntekijöille oletusarvoisesti.

## <a name="report-contents"></a>Raportin sisältö

**Etuusilmoitus** tulostaa työntekijän vahvistetut suunnitelmavalinnat, myös mahdolliset peruutetut suunnitelmat. Seuraavassa kuvassa tämän raportin esimerkki. 

![Etuusilmoitus](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Raportissa näkyy **suunnitelma**, **kattavuusasetus**, **työntekijän kustannukset** ja **työnantajan kustannukset**. Raportissa on myös luettelo mahdollisista huollettavista. Jos suunnitelmaan on liitetty edunsaajia, edunsaajat sekä heidän prioriteettinsa ja osuus jakaumasta on näkyvissä.

**Etuusilmoitus**-raporttiin voidaan tulostaa samanaikaisesti useita työntekijöitä käyttämällä **Etuusilmoitus**-sivun **Sisällytettävät tietueet** -pikavälilehteä.

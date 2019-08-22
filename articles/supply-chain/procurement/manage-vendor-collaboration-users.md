---
title: Toimittajayhteistyön käyttäjien hallinta
description: Tässä aiheessa kuvataan, miten voit pyytää uusien toimittajayhteistyön käyttäjien valmistelua ja miten uusia toimittajayhteistyön yhteyshenkilöitä lisätään.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d0644372944b4c9d472ff738258665544fccbad4
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742467"
---
# <a name="manage-vendor-collaboration-users"></a>Toimittajayhteistyön käyttäjien hallinta

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten voit pyytää uusien toimittajayhteistyön käyttäjien valmistelua ja miten uusia toimittajayhteistyön yhteyshenkilöitä lisätään. 

Microsoft Dynamics 365 for Finance and Operationsin toimittajayhteistyöliittymästä saadaan tietoja ostotilauksista, laskuista ja lähetysvarastosta ulkoisille toimittajille. Voit luoda uusia toimittajayhteistyön yhteyshenkilöitä ja pyytää, että uusia käyttäjiä valmistellaan, jos työskentelet ulkoisena toimittajana **Toimittajan järjestelmänvalvoja (ulkoinen)** -käyttöoikeusroolissa tai vastaavilla käyttöoikeuksilla. Voit myös suorittaa nämä tehtävät, jos työskentelet hankinta-asiantuntijana Tässä ohjeaiheessa kyseinen rooli viittaa hankinta-asiantuntijaan, joka toimii Finance and Operations -esiintymän omistamassa yrityksessä. Katso lisätietoja toimittajayhteistyön käytöstä ulkoisena toimittajana kohdasta [Toimittajayhteistyö asiakkaiden kanssa](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Katso lisätietoja toimittajayhteistyön käytöstä hankinta-asiantuntijana kohdasta [Toimittajayhteistyö ulkoisten toimittajien kanssa](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Lisää uusia toimittajayhteistyön yhteyshenkilöitä
Jos haluat antaa toimittajayhteistyön käyttöoikeudet toiselle käyttäjälle, heidät on ensin lisättävätoimittajayhteistyön yhteyshenkilöiksi. Voit myös halutessasi lisätä yhteyshenkilöitä yrityksesi työntekijöille, jotka eivät käytä toimittajayhteistyötä. He voivat olla yhteyshenkilöitä esimerkiksi toisentyyppisiä hankintatietoja varten. Uudet yhteystiedot lisätään **Kaikki yhteyshenkilöt** -sivulle, jolle päästään **Toimittajayhteistyö** &gt; **Yhteyshenkilöt** -valikosta. Uuden yhteyshenkilön lisääminen:

1.  Valitse **Uusi**.
2.  Anna yhteyshenkilön tiedot.
3.  Valitse oikeushenkilö, jota he edustavat yrityksessäsi, ja minkä oikeushenkilön kanssa he tekevät yhteistyötä yrityksessä. Voit tehdä tämän valitsemalla **Oikeushenkilö omassa yrityksessä**/**Oikeushenkilö asiakasyrityksessä** -parin.
4.  Valitse **Luo**.

Jos haluat poistaa yhteyshenkilön tiedot, voit poistaa vain itse luomasi tiedot.

## <a name="vendor-collaboration-user-requests"></a>Toimittajayhteistyön käyttäjäpyynnöt
Toimittajayhteistyön käyttäjäpyyntöjä voi esittää hankinta-asiantuntija tai ulkoisen toimittajan järjestelmänvalvoja.

-   Jos olet ulkoinen toimittaja, lähetä pyynnöt **Kaikki yhteyshenkilöt** -sivulta **Toimittajayhteistyö**-moduulista.
-   Jos olet hankinta-asiantuntija, lähetä pyynnöt **Tarkastele yhteyshenkilöitä** -sivulta. Voit tehdä tämän valitsemalla toimittajatietueessa siirtymisruudun **Asetukset** osassa, valitsemalla **Yhteyshenkilöt** &gt; **Tarkastele yhteyshenkilöitä**.

Voit tehdä pyynnön käyttäjän valmistelemisesta, käyttäjän poistamisesta tai käyttöoikeusroolien muokkaamisesta. Jos olet ulkoisen toimittajan järjestelmänvalvoja, sinun on rekisteröidyttävä yhteyshenkilöksi toimittajatileille, joille haluat tehdä käyttäjän pyyntöjä, ja sinulla on oltava toimittajayhteistyöliittymän käyttöoikeudet näiltä toimittajatileiltä.  

Kun pyyntö on lähetetty, se lisätään **Toimittajayhteistyön käyttäjäpyynnöt** -luetteloon **Toimittajayhteistyö**-moduuliin, ja **Toimittajayhteistyön käyttäjäpyyntö** -luetteloon **Hankinta**-moduulissa (hankintamoduuli ei ole ulkoisten käyttäjien käytettävissä).

### <a name="provision-a-user"></a>Käyttäjän valmistelu

Ennen kuin voit pyytää uuden käyttäjän valmistelua, kyseisen henkilön on määritettävä yhteyshenkilöksi vähintään yhdelle toimittajatilille. Uuden toimittajayhteistyön käyttäjäpyynnön luominen:

1. **Kaikki yhteyshenkilöt** -sivulla valitse **Valmistele toimittajakäyttäjä**.
2. Anna käyttäjän sähköpostiosoite. Käyttäjä käyttää tätä osoitetta kirjautuessaan Finance and Operationsiin. Jos sähköpostiosoite kuuluu Microsoft Azuren vuokraajaksi rekisteröityneelle toimialueelle, sähköpostiosoitteen tulee olla aiemmin luodulla Azure Active Directory (AAD) -tilillä, jotta valmisteluprosessi onnistuu. Jos sähköpostiosoite kuuluu Microsoft Azuren vuokraajaksi rekisteröityneelle toimialueelle, AAD-tili luodaan käyttöoikeuden valmisteluprosessin aikana ja uusi käyttäjä saa kutsuviestin. Kuluttaja-asiakkaiden sähköpostiosoitteita, joiden verkkotunnus on esimerkiksi @hotmail.com, @gmail.com tai @comcast.net, ei voida käyttää rekisteröidyttäessä Finance and Operations -käyttäjäksi.
3. Määritä **Toimittajayhteistyön käyttö sallittu** -asetukseksi **Kyllä** kaikkille yrityksille, joihin käyttäjä tarvitsee käyttöoikeudet.
4. **Määritä käyttäjärooleja** -osassa valitse **Määritä** -valintaruutu niille käyttöoikeusrooleille, jotka uusi käyttäjä tarvitsee.
5. Valitse **Lähetä**.

Kun toimittajan käyttäjäpyyntö on lähetetty **Toimittajayhteistyön käyttö sallittu** -kentän arvoksi tulee **Kyllä** valitulle toimittajatilille ja käyttäjäpyynnön työnkulku aloitetaan. Uusi käyttäjä luodaan Finance and Operationsissa ja käyttöoikeusroolit määritetään osana työnkulkua. Lisäksi Azure B2B -palvelu aktivoituu ja käynnistää käsittelyn Azure-portaalissa ja liittää uuden tai entisen ADD-käyttäjätilin Finance and Operationsin käyttäjätiliin. Lisätietoja on kohdassa [Azure AD B2B -yhteistyö](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Poista käyttäjä

Toimittajayhteistyön käyttöoikeus voidaan poistaa käyttäjältä kahdella tavalla:

-   Toimittajan **Yhteyshenkilöt**-sivulla määritä **Toimittajayhteistyön käyttö sallittu** -asetukseksi **ei** yhteyshenkilölle. Tämä voidaan tehdä yksitellen yrityksessä, joka yhteyshenkilö käyttäjä on. Tätä vaihtoehtoa voivat käyttää vain hankinta-asiantuntijat.
-   Poista koko käyttäjätili käytöstä lähettämällä **Poista toimittajakäyttäjä käytöstä** -pyyntö.

Käyttäjän käyttöoikeuksien poistamispyynnön esittäminen:

1.  **Kaikki yhteyshenkilöt** -sivulla valitse **Poista** **toimittajakäyttäjä**.
2.  Kirjoita kommentti **Liiketoimintaperuste**-kentässä.
3.  Valitse **Lähetä**.

### <a name="modify-security-roles"></a>Muuta käyttöoikeusrooleja

**Ylläpidä toimittajakäyttäjän rooleja** -sivu on sama kuin **Valmistele toimittajakäyttäjä** -sivu sillä erotuksella, että käyttöoikeusrooliluetteloa voidaan muokata.  

Voit pyytää käyttöoikeusroolien muokkaamista käyttäjälle seuraavasti:

1.  **Kaikki yhteyshenkilöt** -sivulla valitse **Ylläpidä** **toimittajakäyttäjän** rooleja.
2.  Kirjoita kommentti **Liiketoimintaperuste**-kentässä.
3.  Valitse **Ylläpidä käyttäjärooleja** -osa, valitse käyttöoikeusroolit, jotka haluat liittää tai poistaa.
4.  Valitse **Lähetä**.





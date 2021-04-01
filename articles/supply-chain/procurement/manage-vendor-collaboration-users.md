---
title: Toimittajayhteistyön käyttäjien hallinta
description: Tässä aiheessa kuvataan, miten voit pyytää uusien toimittajayhteistyön käyttäjien valmistelua ja miten uusia toimittajayhteistyön yhteyshenkilöitä lisätään.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 18403c336253a9b2e85128329ac03daf081cd560
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244132"
---
# <a name="manage-vendor-collaboration-users"></a>Toimittajayhteistyön käyttäjien hallinta

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten voit pyytää uusien toimittajayhteistyön käyttäjien valmistelua ja miten uusia toimittajayhteistyön yhteyshenkilöitä lisätään. 

Dynamics 365 Supply Chain Managementin toimittajayhteistyöliittymästä saadaan tietoja ostotilauksista, laskuista ja lähetysvarastosta ulkoisille toimittajille. Voit luoda uusia toimittajayhteistyön yhteyshenkilöitä ja pyytää, että uusia käyttäjiä valmistellaan, jos työskentelet ulkoisena toimittajana **Toimittajan järjestelmänvalvoja (ulkoinen)** -käyttöoikeusroolissa tai vastaavilla käyttöoikeuksilla. Voit myös suorittaa nämä tehtävät, jos työskentelet hankinta-asiantuntijana Tässä ohjeaiheessa kyseinen rooli viittaa hankinta-asiantuntijaan, joka toimii Supply Chain Management -esiintymän omistamassa yrityksessä. Lisätietoja toimittajayhteistyön käytöstä ulkoisena toimittajana on kohdassa [Toimittajayhteistyö asiakkaiden kanssa](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Lisätietoja toimittajayhteistyön käytöstä hankinta-asiantuntijana on kohdassa [Toimittajayhteistyö ulkoisten toimittajien kanssa](vendor-collaboration-work-external-vendors.md).

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
-   Jos olet hankinta-asiantuntija, lähetä pyynnöt **Tarkastele yhteyshenkilöitä** -sivulta. Voit tehdä tämän valitsemalla toimittajatietueessa toimintoruudussa **Asetukset** ja valitsemalla sitten **Yhteyshenkilöt** &gt; **Tarkastele yhteyshenkilöitä**.

Voit tehdä pyynnön käyttäjän valmistelemisesta, käyttäjän poistamisesta tai käyttöoikeusroolien muokkaamisesta. Jos olet ulkoisen toimittajan järjestelmänvalvoja, sinun on rekisteröidyttävä yhteyshenkilöksi toimittajatileille, joille haluat tehdä käyttäjän pyyntöjä, ja sinulla on oltava toimittajayhteistyöliittymän käyttöoikeudet näiltä toimittajatileiltä.  

Kun pyyntö on lähetetty, se lisätään **Toimittajayhteistyön käyttäjäpyynnöt** -luetteloon **Toimittajayhteistyö**-moduuliin, ja **Toimittajayhteistyön käyttäjäpyyntö** -luetteloon **Hankinta**-moduulissa (hankintamoduuli ei ole ulkoisten käyttäjien käytettävissä).

### <a name="provision-a-user"></a>Käyttäjän valmistelu

Ennen kuin voit pyytää uuden käyttäjän valmistelua, kyseisen henkilön on määritettävä yhteyshenkilöksi vähintään yhdelle toimittajatilille. Uuden toimittajayhteistyön käyttäjäpyynnön luominen:

1. **Kaikki yhteyshenkilöt** -sivulla valitse **Valmistele toimittajakäyttäjä**.
2. Anna käyttäjän sähköpostiosoite. Käyttäjä voi käyttää tätä osoitetta Supply Chain Managementiin kirjautumiseen. Jos sähköpostiosoite kuuluu Microsoft Azuren vuokraajaksi rekisteröityneelle toimialueelle, sähköpostiosoitteen tulee olla aiemmin luodulla Azure Active Directory (AAD) -tilillä, jotta valmisteluprosessi onnistuu. Jos sähköpostiosoite kuuluu Microsoft Azuren vuokraajaksi rekisteröityneelle toimialueelle, AAD-tili luodaan käyttöoikeuden valmisteluprosessin aikana ja uusi käyttäjä saa kutsuviestin. Kuluttaja-asiakkaiden sähköpostiosoitteita, joiden verkkotunnus on esimerkiksi @hotmail.com, @gmail.com tai @comcast.net, ei voida käyttää rekisteröidyttäessä käyttäjäksi.
3. Määritä **Toimittajayhteistyön käyttö sallittu** -asetukseksi **Kyllä** kaikkille yrityksille, joihin käyttäjä tarvitsee käyttöoikeudet.
4. **Määritä käyttäjärooleja** -osassa valitse **Määritä** -valintaruutu niille käyttöoikeusrooleille, jotka uusi käyttäjä tarvitsee.
5. Valitse **Lähetä**.

Kun toimittajan käyttäjäpyyntö on lähetetty **Toimittajayhteistyön käyttö sallittu** -kentän arvoksi tulee **Kyllä** valitulle toimittajatilille ja käyttäjäpyynnön työnkulku aloitetaan. Uusi käyttäjä luodaan ja käyttöoikeusroolit määritetään osana työnkulkua. Lisäksi Azure B2B -palvelu aktivoituu ja käynnistää käsittelyn Azure-portaalissa ja liittää uuden tai entisen ADD-käyttäjätilin Supply Chain Managementin käyttäjätiliin. Lisätietoja on kohdassa [Azure AD B2B -yhteistyö](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
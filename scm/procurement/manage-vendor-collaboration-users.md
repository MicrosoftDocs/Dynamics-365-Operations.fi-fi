---
title: "Toimittajayhteistyön käyttäjien hallinta"
description: "Tässä aiheessa kuvataan, miten voit pyytää uusien toimittajayhteistyön käyttäjien valmistelua ja miten uusia toimittajayhteistyön yhteyshenkilöitä lisätään."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>Toimittajayhteistyön käyttäjien hallinta

Tässä aiheessa kuvataan, miten voit pyytää uusien toimittajayhteistyön käyttäjien valmistelua ja miten uusia toimittajayhteistyön yhteyshenkilöitä lisätään. 

Microsoft Dynamics 365 for Operations - toimittajayhteistyöliittymästä saadaan tietoja ostotilauksista, laskuista ja lähetysvarastosta ulkoisille toimittajille. Voit luoda uusia toimittajayhteistyön yhteyshenkilöitä ja pyytää, että uusia käyttäjiä valmistellaan, jos työskentelet ulkoisena toimittajana **Toimittajan järjestelmänvalvoja (ulkoinen)** -käyttöoikeusroolissa tai vastaavilla käyttöoikeuksilla. Voit myös suorittaa nämä tehtävät, jos työskentelet hankinta-asiantuntijana Tässä aiheessa kyseinen rooli viittaa hankinta-asiantuntijaan, joka toimii yrityksessä, joka omistaa Dynamics 365 for Operations -esiintymän. Saat lisätietoja siitä, miten käyttää yhteistyössä toimittaja, jos olet ulkoinen toimittaja [toimittaja asiakkaiden kanssa](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Saat lisätietoja käyttämisestä Jos hankintaan, joka on ammatillinen toimittaja, yhteistyössä [toimittaja yhteistyössä ulkoisten toimittajien,](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Lisää uusia toimittajayhteistyön yhteyshenkilöitä
Jos haluat antaa toimittajayhteistyön käyttöoikeudet toiselle käyttäjälle, heidät on ensin lisättävätoimittajayhteistyön yhteyshenkilöiksi. Voit myös halutessasi lisätä yhteyshenkilöitä yrityksesi työntekijöille, jotka eivät käytä toimittajayhteistyötä. He voivat olla yhteyshenkilöitä esimerkiksi toisentyyppisiä hankintatietoja varten. Uudet yhteystiedot lisätään **kaikki yhteystiedot** sivu, joka voidaan avata **toimittaja, yhteistyössä**&gt;**yhteystiedot** valikosta. Uuden yhteyshenkilön lisääminen:

1.  Valitse **Uusi**.
2.  Anna yhteyshenkilön tiedot.
3.  Valitse oikeushenkilö, jota he edustavat yrityksessäsi, ja minkä oikeushenkilön kanssa he tekevät yhteistyötä yrityksessä. Voit tehdä tämän valitsemalla **oikeushenkilö oman yrityksen**/**oikeushenkilön asiakkaan yrityksen** pari.
4.  Valitse **Luo**.

Jos haluat poistaa yhteyshenkilön tiedot, voit poistaa vain itse luomasi tiedot.

## <a name="vendor-collaboration-user-requests"></a>Toimittajayhteistyön käyttäjäpyynnöt
Toimittajayhteistyön käyttäjäpyyntöjä voi esittää hankinta-asiantuntija tai ulkoisen toimittajan järjestelmänvalvoja.

-   Jos olet ulkoinen toimittaja, voit lähettää pyyntöjä **kaikki yhteystiedot** sivun sisällä **toimittaja, yhteistyössä** moduuli.
-   Jos olet hankinta-asiantuntija, lähetä pyynnöt **Tarkastele yhteyshenkilöitä** -sivulta. Voit tehdä tämän valitsemalla toimittajan tietueeseen, joka **asennus** toiminto-ruudussa, valitse-osassa **yhteystiedot**&gt;**tarkastella yhteystietoja**.

Voit tehdä pyynnön käyttäjän valmistelemisesta, käyttäjän poistamisesta tai käyttöoikeusroolien muokkaamisesta. Jos olet ulkoisen toimittajan järjestelmänvalvoja, sinun on rekisteröidyttävä yhteyshenkilöksi toimittajatileille, joille haluat tehdä käyttäjän pyyntöjä, ja sinulla on oltava toimittajayhteistyöliittymän käyttöoikeudet näiltä toimittajatileiltä.  

Kun pyyntö on lähetetty, se lisätään **Toimittajayhteistyön käyttäjäpyynnöt** -luetteloon **Toimittajayhteistyö**-moduuliin, ja **Toimittajayhteistyön käyttäjäpyyntö** -luetteloon **Hankinta**-moduulissa (hankintamoduuli ei ole ulkoisten käyttäjien käytettävissä).

### <a name="provision-a-user"></a>Käyttäjän valmistelu

Ennen kuin voit pyytää uuden käyttäjän valmistelua, kyseisen henkilön on määritettävä yhteyshenkilöksi vähintään yhdelle toimittajatilille. Uuden toimittajayhteistyön käyttäjäpyynnön luominen:

1.  - **Kaikki yhteystiedot** -sivulla **tarjotaan toimittajakäyttäjän**.
2.  Anna käyttäjän sähköpostiosoite. Käyttäjä käyttää tätä osoitetta kirjautuessaan Dynamics 365 for Operations -järjestelmään. Jos sähköpostiosoite kuuluu Microsoft Azuren vuokraajaksi rekisteröityneelle toimialueelle, sähköpostiosoitteen tulee olla aiemmin luodulla Azure Active Directory (ADD) -tilillä, jotta valmisteluprosessi onnistuu. Jos sähköpostiosoite kuuluu Microsoft Azuren vuokraajaksi rekisteröityneelle toimialueelle, ADD-tili luodaan käyttöoikeuden valmisteluprosessin aikana ja uusi käyttäjä saa kutsuviestin. Kuluttaja email osoitteet-toimialueiden kanssa kuten @hotmail.com, @gmail.com, tai @comcast.netei voi rekisteröidä Dynamics-365 toimintoja käyttäjälle.
3.  Määritä **Toimittajayhteistyön käyttö sallittu** -asetukseksi **Kyllä** kaikkille yrityksille, joihin käyttäjä tarvitsee käyttöoikeudet.
4.  - **Määritä käyttäjärooleja** -osassa valitse **Määritä** -valintaruutu niille käyttöoikeusrooleille, jotka uusi käyttäjä tarvitsee.
5.  Valitse **Lähetä**.

Toimittajan käyttäjäpyyntö lähetettäessä **toimittaja yhteistyö käyttö sallittu** -kentän arvoksi **Kyllä**, ja valitun toimittajatilin käyttäjä pyytää työnkulku on aloitettu. Uusi käyttäjä luodaan Dynamics 365 for Operations -järjestelmässä ja suojausroolit määritetään osana työnkulkua. Lisäksi Azure B2B -palvelu aktivoituu ja käynnistää käsittelyn Azure-portaalissa ja liittää uuden tai entisen ADD-käyttäjätilin Dynamics 365 for Operations -käyttäjätiliin.

### <a name="inactivate-a-user"></a>Poista käyttäjä

Toimittajayhteistyön käyttöoikeus voidaan poistaa käyttäjältä kahdella tavalla:

-   Toimittajan **Yhteyshenkilöt**-sivulla määritä **Toimittajayhteistyön käyttö sallittu** -asetukseksi **ei** yhteyshenkilölle. Tämä voidaan tehdä yksitellen yrityksessä, joka yhteyshenkilö käyttäjä on. Tätä vaihtoehtoa voivat käyttää vain hankinta-asiantuntijat.
-   Poista koko käyttäjätili käytöstä lähettämällä **Poista toimittajakäyttäjä käytöstä** -pyyntö.

Voit pyytää, että käyttäjä poistaa käytöstä seuraavasti:

1.  - **Kaikki** -sivulla **Poista käytöstä****toimittajakäyttäjän**.
2.  Kirjoita kommentti **Liiketoimintaperuste**-kentässä.
3.  Valitse **Lähetä**.

### <a name="modify-security-roles"></a>Muuta käyttöoikeusrooleja

**Ylläpidä toimittajan käyttäjäroolien** sivulla on sama kuin **tarjotaan toimittajakäyttäjän** sivu, paitsi että käyttöoikeusroolien luetteloa voidaan muokata.  

Voit pyytää käyttöoikeusroolit muokataan käyttäjän seuraavasti:

1.  - **Kaikki yhteystiedot** -sivulla **ylläpitäminen****toimittaja käyttäjien roolien**.
2.  Kirjoita kommentti **Liiketoimintaperuste**-kentässä.
3.  Valitse **Ylläpidä käyttäjärooleja** -osa, valitse käyttöoikeusroolit, jotka haluat liittää tai poistaa.
4.  Click **Submit**.




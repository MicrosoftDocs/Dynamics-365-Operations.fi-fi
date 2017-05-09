---
title: "Määritä yrityskohtaisia henkilöstöhallinnon parametreja"
description: "Jotkin henkilöstöhallinnon (HR) parametrien asetukset ovat yhteisiä eri yrityksissä, toiset taas yrityskohtaisia. Tässä artikkelissa on selostettu, miten määritetään yrityskohtaisia henkilöstöhallinnon parametreja."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: aaf5c93a1ac71de27338c13218407616808ee001
ms.openlocfilehash: 39f2904a6b722ad0048ba1d94651098ee642079b
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-company-specific-hr-parameters"></a>Määritä yrityskohtaisia henkilöstöhallinnon parametreja

[!include[banner](includes/banner.md)]


Jotkin henkilöstöhallinnon (HR) parametrien asetukset ovat yhteisiä eri yrityksissä, toiset taas yrityskohtaisia. Tässä artikkelissa on selostettu, miten määritetään yrityskohtaisia henkilöstöhallinnon parametreja.

Henkilöstöhallinto (HR)-parametrien määrittämiseen käytetään kahta sivua. Käytä yhtiöiden kesken jaettujen parametrien määrittämiseen **Henkilöstöhallinnon jaetut parametrit** -sivua. Käytä yhtiökohtaisten (ts. asetukset koskevat yhtä yhtiötä) parametrien määrittämiseen **Henkilöstöparametrit**-sivua. **Henkilöstöparametrit**-sivulla asetukset jaetaan kuudelle välilehdelle:

-   Yleinen
-   Työhönotto
-   Kompensaatio
-   Numerojärjestykset
-   Perhe ja sairauspoissaolon säädös (FMLA)
-   Työntekijän itsepalvelu

Kukin välilehti sisältää yksittäistä yhtiötä koskevia tietoja. **Yleinen**-välilehdellä määritetään poissaoloja, tapaturmia ja sairaustapauksia sekä uusia työntekijöitä koskevien tietojen ulkonäkö. Tämän välilehden asetukset määrittävät myös osan oletusarvoista, jotka tulevat näkyviin työskentelysi aikana. Tarkemmin sanoen, tällä välilehdellä voit valita avoimissa poissaolotapahtumissa käytettävän värin, määrittää raporteissa käytettävän tyylitiedoston, määrittää, otetaanko integrointi käyttöön koulutusten ja poissaolomerkintöjen välillä, ja valita tämän integroinnin hallinnassa käytettävä poissaolokoodi. Voit myös määrittää, miten pitkään loukkaantumis- ja sairaustapauksia säilytetään, ja määrittää oletusarvoisen tunnusnumeron, joka näytetään, kun uusi työntekijä palkataan. 

**Työhönotto**-välilehden asetuksilla määritetään tiedostotyypit, joita käytetään automaattisessa hakijoiden kanssa käytävässä yhteydenpidossa sekä avoimissa hakemuksissa (hakemuksissa, jotka eivät koske määrättyä työhönottoprojektia) käytettävän työhönottoprojekti. Työhönottoprosessin vanhentumisasetuksissa määritetty ajanjakso määrittää ne työhönottoprojektit, jotka sisällytetään **Vanhentuvat projektit** -ruudulle **Työhönoton hallinta** -työtilassa. Hakemuksen määräajan varoitukselle määritettyä ajanjaksoa käytetään näyttämään ne työhönottoprojektit, jotka lähestyvät hakemuksille asetettua määräaikaansa **Hakemuksen määräaika lähestyy** -ruudulla **Työhönotto**-työtilassa. 

**Kompensaatio**-välilehden asetukset määrittävät, onko käyttäjien vahvistettava, että he haluavat tallentaa joko kiinteän tai muuttuvan kompensaatiosuunnitelman asetukset. Jos valitset **Otetaan vahvistuksen tallennus käyttöön** -asetuksen, aina kun käyttäjä sulkee kompensaatioon liittyvän sivun, tälle lähetetään viesti, jossa tätä pyydetään tallentamaan tietue. Jotkin kompensaationhallinnan sivut eivät salli käyttäjille tietojen poistamista. Näin ollen, kehottamalla käyttäjiä vahvistamaan, että he haluavat tallentaa tiedot, saatat pystyä rajoittamaan tietojen määrää, jotka on tallennettu mutta joita ei voida poistaa myöhemmin. Jos **Otetaan vahvistuksen tallennus käyttöön** -valintaruutu tyhjennetään, tietueet tallennetaan aina heti, mahdollisesti jo ennen kuin käyttäjä on valmis. Jos käytät suorituskyvyn hallintaa, **Kompensaatio** -välilehdellä voit myös valita suorituskykyä arvioitaessa käytettävän arviointimallin kompensaatiosuunnitelmille määritetyn mallin asemesta. 

**Numerojärjestys**-välilehden asetukset määrittävät numerosarjat, joita käytetään tunnusten määrittämiseen automaattisesti nimikkeille henkilöstöhallinnossa, kuten sovelluksille, poissaolomerkinnöille, kompensaatioprosessin tuloksille, tapausnumeroille, kursseille ja kurssien työjärjestyksille. Jos haluat ylläpitää numerosarjaviitteitä ja koodeja, käytä **Numerojärjestykset**-luettelosivua (valitse **Organisaation hallinto** &gt; **Numerojärjestykset** &gt; **Numerojärjestykset**). 

**FMLA**-välilehden asetuksissa määritetään, montako tuntia työntekijän on työskenneltävä saadakseen oikeuden FMLA-etuihin, oikeuteen vaadittavan työsuhteen pituuden, ja työsuhteen alkamispäivän, jota käytetään määrittämään työsuhteen pituus. Asetukset määrittävät myös FMLA-tuntien määrän, joihin työntekijällä on oikeus, ja FMLA-lomakalenterin, jota käytetään työntekijöiden käyttämien FMLA-tuntien määrän laskemisessa. **FMLA**-välilehti koskee vain yhdysvaltalaisia yrityksiä. 

**Huomautus:** Tehtyjen työtuntien määrä ei voi ylittää 1 250 tuntia, ja työsuhteen pituus ei voi ylittää 12 kuukautta. Nämä enimmäisarvot ovat Yhdysvaltojen liittovaltion lainsäädännön mukaiset. Lopuksi, **Työntekijän itsepalvelu** -välilehden asetuksissa määritellään tiedot, jotka esimies voi syöttää työntekijöidensä puolesta.

<a name="see-also"></a>Lisätietoja
--------

[Määritä henkilöstöhallinnon parametreja eri yrityksissä](set-up-hr-parameters-across-legal-entities.md)





---
title: Loma- ja poissaoloparametrien määrittäminen
description: Määritä henkilöstöhallinnon parametrit lomaa ja poissaoloa varten Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db96073f0a16f1c710fbfebb2d08a1d693eab1e1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463379"
---
# <a name="configure-leave-and-absence-parameters"></a>Loma- ja poissaoloparametrien määrittäminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ennen kuin määrität loma- ja poissaolosuunnitelmat Dynamics 365 Human Resources -ohjelmassa, kannattaa tarkistaa kaikkien liittyvien henkilöstöparametrien asetukset, kuten esimerkiksi seuraavat:

- Lomapyyntöjen numerosarja
- Perhe- ja sairauspoissaolon säädös (FMLA) -asetukset
- Työntekijän itsepalvelun asetukset loma- ja poissaolopyynnöille
- Loman ja poissaolon parametrit

## <a name="view-and-change-human-resources-parameters"></a>Tarkastele ja muuta henkilöstöparametreja

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Määritys**-kohdasta **Henkilöstöparametrit**.

3. Tarkista **Numerosarjat**-välilehdessä **Numerosarjakoodi** **Lomapyynnön tunnusta** varten ja muuta tarvittaessa. Tämä asetus määrittää järjestyksen, jota käytetään automaattisesti, kun tunnuksia annetaan lomapyyntöjä varten.

4. Tarkista **FMLA**-välilehdessä FMLA-asetukset ja muuta niitä tarvittaessa.

5. Määritä **Työntekijän itsepalvelu** -välilehdessä, voivatko esimiehet kirjoittaa loma- ja poissaolopyyntöjä työntekijöidensä puolesta.

7. Valitse **Tallenna**.

>[!IMPORTANT]
>Loman ja poissaolon tarkasteleminen yrityksissä tapahtuu nyt esikatselussa. Se on otettava käyttöön **eristysympäristössä**, jotta loma- ja poissaolovaihtoehto otetaan käyttöön. Lisätietoja esiversio-ominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>Human Resourcesin jaettujen parametrien tarkastelemien ja muuttaminen

1. Valitse **Henkilöstön hallinta** -sivulla **Linkit**-välilehti.

2. Valitse **Määritys**-kohdasta **Human resourcesin jaetut parametrit**.

3. Valitse **Laajennetut käyttöoikeudet** -välilehdessä **Kyllä** **Ota käyttöön yritystenvälinen lomanäkymä** -kohdassa, jos haluat loman olevan tarkasteltavissa eri yrityksissä.

4. Valitse **Tallenna**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Loma- ja poissaoloparametrien tarkasteleminen ja muuttaminen

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Asetukset**-kohdasta **Loma- ja poissaoloparametrit**.

3. Määritä **Yleiset**-välilehdessä seuraavat parametrit:
 
    - Määritä **Loma-ja poissaoloyksikkö** joko tunteina tai päivinä. Jos valinta on päivät, voit valita **Ota käyttöön puolipäiväiset määritykset**, jolloin työntekijät voivat valita joko ensimmäisen tai toisen puolen päivästä lomapyynnöille. 

    - Valitse **Palvelukuukausien voimaantulopäivä**, kun haluat määrittää, milloin jaksotusprosentit tulevat voimaan palvelukuukausien avulla.

    - Valitse **Saldon laskeminen**, kun haluat näyttää saldon kuluvan päivän ja jaksotuskauden mukaan. Jos valitset **Saldo tänään** -vaihtoehdon, saldo näyttää kaikkien kertymien, oikaisujen ja pyyntöjen kokonaissumman tänään. Jos valitset **Saldo jaksotuskaudelta**, saldo näyttää kaikkien jaksotusten, oikaisujen ja pyyntöjen kokonaissumman niiden jaksotuskauden mukaan, jotka on määritetty lomasuunnitelman frekvenssin mukaan. 

    - Määritä siirtokirjauksen tekemisen vanhentumisen erätyön aloitusaika.  
    
    - Valitse **Työntekijät voivat ostaa lomaa**- ja **Salli työntekijöiden myydä lomaa** -kohdissa **Kyllä**. Jos valitse näissä vaihtoehdoissa **Kyllä**, voit luoda käytännöt loman vaihtamisesta rahaksi ja lomapalkan vaihtamisesta vapaaksi ja antaa työntekijöille mahdollisuuden lähettää loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjä.

## <a name="configure-calendar-parameters"></a>Määritä kalenteriparametrit

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Asetukset**-kohdasta **Loma- ja poissaoloparametrit**.

3. Muuta **Kalenteri**-välilehdessä asetukset tarvittaessa.

4. Valitse **Tallenna**.

## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
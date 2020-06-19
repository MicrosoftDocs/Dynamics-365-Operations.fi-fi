---
title: Loma- ja poissaoloparametrien määrittäminen
description: Määritä henkilöstöhallinnon parametrit lomaa ja poissaoloa varten Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: 5e4d3b3e4b373631bed5e2d7e3c3a4e14f0c5c98
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428941"
---
# <a name="configure-leave-and-absence-parameters"></a>Loma- ja poissaoloparametrien määrittäminen

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

6. Tarkista **Loma ja poissaolo** -välilehdessä asetukset ja muuta niitä tarvittaessa.

7. Valitse **Tallenna**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Loma- ja poissaoloparametrien tarkasteleminen ja muuttaminen

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Asetukset**-kohdasta **Loma- ja poissaoloparametrit**.

3. Määritä **Yleiset**-välilehdessä seuraavat parametrit:
 
    - Määritä **Loma-ja poissaoloyksikkö** joko tunteina tai päivinä. Jos valinta on päivät, voit valita **Ota käyttöön puolipäiväiset määritykset**, jolloin työntekijät voivat valita joko ensimmäisen tai toisen puolen päivästä lomapyynnöille. 

    - Valitse **Palvelukuukausien voimaantulopäivä**, kun haluat määrittää, milloin jaksotusprosentit tulevat voimaan palvelukuukausien avulla.

    - Valitse **Saldon laskeminen**, kun haluat näyttää saldojen näyttämisen tänään tai jaksotuskauden mukaan. Jos valitset **Saldo tänään** -vaihtoehdon, saldo näyttää kaikkien kertymien, oikaisujen ja pyyntöjen kokonaissumman tänään. Jos valitset **Saldo jaksotuskaudelta**, saldo näyttää kaikkien jaksotusten, oikaisujen ja pyyntöjen kokonaissumman niiden jaksotuskauden mukaan, jotka on määritetty lomasuunnitelman frekvenssin mukaan. 

## <a name="configure-calendar-parameters"></a>Määritä kalenteriparametrit

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Asetukset**-kohdasta **Loma- ja poissaoloparametrit**.

3. Muuta **Kalenteri**-välilehdessä asetukset tarvittaessa.

4. Valitse **Tallenna**.

## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)

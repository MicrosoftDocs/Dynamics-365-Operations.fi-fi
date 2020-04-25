---
title: Määritä loman ja poissaolon tyypit
description: Määritä Dynamics 365 Human Resourcesissa lomatyypit, joita työntekijät voivat valita.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198047"
---
# <a name="configure-leave-and-absence-types"></a>Määritä loman ja poissaolon tyypit

Lomatyypit Dynamics 365 Human Resourcesissa määrittävät erilaiset poissaolotyypit, joita työntekijät voivat ilmoittaa. Voit räätälöidä lomatyyppejä organisaatiosi tarpeiden mukaan. Esimerkkejä lomatyypeistä:

- Palkallinen vapaa (PTO)
- Palkaton vapaa
- Palkallinen vapaa
- Sairausloma
- Sairausloma
- Perheloma
- Lyhytaikainen vamma
- Suruvapaa

## <a name="add-a-leave-type"></a>Lomatyypin lisääminen

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Asetukset**-kohdasta **Loma- ja poissaolotyypit**.

3. Valitse **Uusi**.

4. Kirjoita lomatyypin nimi **Tyyppi**-kohtaan, valitse työnkulku **Työnkulun tunnus** -kohdasta ja kirjoita kuvaus **Kuvaus**-kohtaan.

5. Valitse **Yleinen**-kohdasta **Ei mitään**, **Ajoitettu** tai **Ennakoimaton** **Luokan** avattavasta luettelosta.

6. Valitse ansaitsemiskoodi avattavasta **Ansaitsemiskoodi**-valikosta.

7. Valitse **Vaadittu syykoodi** -kohdassa, haluatko vaatia syykoodin. Jos haluat vaatia syykoodeja, ne on ehkä lisättävä. Valitse **Syykoodit**-kohdasta **Lisää**, valitse syykoodi ja valitse sitten sen vieressä oleva **Käytössä** valintaruutu.

8. Valitse **Rajoita käyttöoikeuksia valittuihin rooleihin** -kohdassa, haluatko rajoittaa käyttöä. Valitse sitten käyttöoikeusroolit **Tämän lomatyypin käyttöoikeusroolit** -kohdasta. Käyttöoikeusroolit määritetään työnkulussa, jonka valitsit **Työnkulun tunnus** -kohdasta aiemmin tässä toimintosarjassa.

9. Valitse **Tallenna**.

## <a name="configure-leave-type-rules"></a>Lomatyypin sääntöjen määrittäminen

1. Määritä lomatyypin pyöristysasetukset. Vaihtoehtoja ovat **Ei mitään**, **Ylös**, **Alas** ja **Lähin**. Voit myös määrittää lomatyypin pyöristystarkkuuden.

2. Määritä lomatyypin **Lomakorjaukset**. Kun valitset tämän vaihtoehdon, henkilöstöhallinto käyttää työpäivään kuuluvien lomien määrää määrittääkseen, miten lomatyypille voidaan jaksottaa aikaa. Jos esimerkiksi joulupäivä osuu maanantaihin, henkilöstöhallinto vähentää yhden päivän lomatyypistä jaksotusten käsittelyn yhteydessä.

   Voit määrittää lomat työaikakalenteriin. Lisätietoja on ohjeaiheessa [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)
   
## <a name="configure-preview-features"></a>Esikatseluominaisuuksien määrittäminen

Jos olet ottanut käyttöön loman ja poissaolon esikatseluominaisuudet, sinun on määritettävä myös niiden asetukset.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Valitse lomatyyppi, johon siirrettävät saldot siirretään. Voit myös luoda uuden lomatyypin siirtokirjauksen. 

## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)
- [Loma- ja poissaolosuunnitelman luominen](hr-leave-and-absence-plans.md)
- [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)

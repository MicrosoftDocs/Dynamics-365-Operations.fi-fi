---
title: Määritä loman ja poissaolon tyypit
description: Määritä Dynamics 365 Human Resourcesissa lomatyypit, joita työntekijät voivat valita.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e4c4b9c83ca648c21ac20bd20b739af8a6b9ed
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271124"
---
# <a name="configure-leave-and-absence-types"></a>Määritä loman ja poissaolon tyypit

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

9. Valitse **Kalenterin väri** -kohdassa, mikä väri näytetään tämän lomatyypin loma- ja poissaolokalentereissa. 

10. Valitse **Keskeytyssuhteet**-kohdassa haluatko, että tämä lomatyyppi keskeyttää toisen lomatyypin tai tulee toisen lomatyypin keskeyttämäksi. Kun poissaoloa koskeva poissaolopyyntö jätetään, keskeytetyn loman tyypiksi luodaan automaattisesti loman keskeytys. 

10. Valitse **Tallenna**.

## <a name="configure-leave-type-rules"></a>Lomatyypin sääntöjen määrittäminen

1. Määritä lomatyypin pyöristysasetukset. Vaihtoehtoja ovat **Ei mitään**, **Ylös**, **Alas** ja **Lähin**. Voit myös määrittää lomatyypin pyöristystarkkuuden.

2. Määritä lomatyypin **Lomakorjaukset**. Kun valitset tämän vaihtoehdon, henkilöstöhallinto käyttää työpäivään kuuluvien lomien määrää määrittääkseen, miten lomatyypille voidaan jaksottaa aikaa. Jos esimerkiksi joulupäivä osuu maanantaihin, henkilöstöhallinto vähentää yhden päivän lomatyypistä jaksotusten käsittelyn yhteydessä.

   Voit määrittää lomat työaikakalenteriin. Lisätietoja on ohjeaiheessa [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)
   
 3. Määritä vapaan tyypiksi **Siirretty lomatyyppi**. Kun valitset tämän vaihtoehdon, kaikki siirrettävät saldot siirretään määritettyyn lomatyyppiin. Siirretyn lomatyypin on sisällyttävä myös loma- ja poissaolosuunnitelmaan. 
 
4. Määritä lomatyypin **vanhenemissäännöt**. Kun määrität tämän asetuksen, voit valita päivien tai kuukausien yksikön ja määrittää vanhenemisajan. Vanhenemisajan voimaantulopäivämäärää käytetään määrittämään, milloin loman vanhenemisen käsittelevä erätyö käynnistetään tai milloin sääntö tulee voimaan. Vanhentuminen tapahtuu aina jaksotuskauden aloituspäivänä. Jos jaksotuskauden alkamispäivämäärä on esimerkiksi 3.8.2021 ja vanhentumissäännöksi on määritetty 6 kuukautta, sääntö käsitellään jaksotuskauden alkamispäivämäärän erääntymisen vastakirjauksen perusteella, joten se suoritetaan 3.2.2022. Kaikki voimassaolon päättymishetkellä jäljellä olevat saldot vähennetään lomatyypistä, ja ne näkyvät lomasaldoissa.
 
## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)
- [Loma- ja poissaolosuunnitelman luominen](hr-leave-and-absence-plans.md)
- [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)
- [Loman keskeyttäminen](hr-leave-and-absence-suspend-leave.md)
- [Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Määritä loman ja poissaolon tyypit
description: Määritä Dynamics 365 Human Resourcesissa lomatyypit, joita työntekijät voivat valita.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e35c5fed886ebf9a453c22b3e04ca9ffe50b6d70
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805201"
---
# <a name="configure-leave-and-absence-types"></a>Määritä loman ja poissaolon tyypit

[!include [preview banner](../includes/preview-banner.md)]

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

1. Valitse **Lomat ja poissaolot** -työtilassa **Linkit**-välilehti.
2. Valitse **Asetukset**-kohdasta **Loma- ja poissaolotyypit**.
3. Valitse **Uusi**.
4. Kirjoita lomatyypin nimi **Tyyppi**-kohtaan , syötä kuvaus **Kuvaus**-kohtaan ja valitse työnkulku **Työnkulun tunnus** -kentästä. Valitse pyyntötyyppi **pyyntötyyppi**-kentässä lomatyypin mukaan. Valitse esimerkiksi **poissaolo** tai **virkavapaa**.
5. Valitse **Yleinen**-kohdasta **Ei mitään**, **Ajoitettu** tai **Ennakoimaton** **Luokan** avattavasta luettelosta.
6. Valitse ansaitsemiskoodi avattavasta **Ansaitsemiskoodi**-valikosta.
7. Valitse **Vaadittu syykoodi** -kohdassa, haluatko vaatia syykoodin. Jos haluat vaatia syykoodeja, ne on ehkä lisättävä. Valitse **Syykoodit**-kohdasta **Lisää**, valitse syykoodi ja valitse sitten sen vieressä oleva **Käytössä** valintaruutu.
8. Jos pyyntötyyppi on **virkavapaa**, toimi seuraavasti:

      1. Valitse kohdassa **kestoltaan avoin**, tulisiko käyttäjillä olla mahdollisuus luoda kestoltaan avoimia lomia.
      2. Jos **kestoltaan avoin** on käytössä, voit valita, tuleeko työntekijöiden lähettää ilmoitus työhön palaamisesta, kun he palaavat lomalta.
      3. Jos työntekijöiden on lähetettävä ilmoitus työhön palaamisesta, voidaan ottaa käyttöön kohta **Ota käyttöön ilmoitus työhön palaamisesta**. Jos **Ota käyttöön ilmoitus työhön palaamisesta** on otettu käyttöön, **Liite pakollinen** on otettu automaattisesti käyttöön, eikä sitä voi ottaa pois käytöstä.

9. Jos käyttäjien on ladattava asiakirjoja, kun he luovat tai päivittävät lomapyyntöjä, voidaan ottaa käyttöön kohta **Liite pakollinen**.
10. Valitse **Rajoita käyttöoikeuksia valittuihin rooleihin** -kohdassa, haluatko rajoittaa käyttöä. Valitse kohdassa **Tämän lomatyypin käyttöoikeusroolit** käyttöoikeusroolit. Käyttöoikeusroolit määritetään työnkulussa, jonka valitsit **Työnkulun tunnus** -kohdasta aiemmin tässä toimintosarjassa.
11. Valitse **Kalenterin väri** -kohdassa, mikä väri näytetään tämän lomatyypin loma- ja poissaolokalentereissa.
11. Valitse **Keskeytyssuhteet**-kohdassa haluatko, että tämä lomatyyppi keskeyttää toisen lomatyypin tai tulee toisen lomatyypin keskeyttämäksi. Kun poissaoloa koskeva poissaolopyyntö jätetään, keskeytetyn loman tyypiksi luodaan automaattisesti loman keskeytys.
12. Valitse **Tallenna**.

## <a name="configure-leave-type-rules"></a>Lomatyypin sääntöjen määrittäminen

1. Määritä **Loma ja poissaolo** -tyypin pyöristysasetukset. Vaihtoehtoja ovat **Ei mitään**, **Ylös**, **Alas** ja **Lähin**. Voit myös määrittää lomatyypin pyöristystarkkuuden.
2. Määritä lomatyypin **Lomakorjaukset**. Kun valitset tämän vaihtoehdon, työpäivään kuuluvien lomien määrää käytetään sen määrittämiseen, miten lomatyypille voidaan jaksottaa aikaa. Jos esimerkiksi joulupäivä osuu maanantaihin, henkilöstöhallinto vähentää yhden päivän lomatyypistä jaksotusten käsittelyn yhteydessä.

   Voit määrittää lomat työaikakalenteriin. Lisätietoja on ohjeaiheessa [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md).
   
 3. Määritä vapaan tyypiksi **Siirretty lomatyyppi**. Kun valitset tämän vaihtoehdon, kaikki siirrettävät saldot siirretään määritettyyn lomatyyppiin. Siirretyn lomatyypin on sisällyttävä myös loma- ja poissaolosuunnitelmaan. 
 
4. Määritä lomatyypin **vanhenemissäännöt**. Kun määrität tämän asetuksen, voit valita päivien tai kuukausien yksikön ja määrittää vanhenemisajan. Vanhenemisajan voimaantulopäivämäärää käytetään määrittämään, milloin loman vanhenemisen käsittelevä erätyö käynnistetään tai milloin sääntö tulee voimaan. Vanhentuminen tapahtuu aina jaksotuskauden aloituspäivänä. Jos jaksotuskauden alkamispäivämäärä on esimerkiksi 3.8.2021 ja vanhentumissäännöksi on määritetty 6 kuukautta, sääntö käsitellään jaksotuskauden alkamispäivämäärän erääntymisen vastakirjauksen perusteella, joten se suoritetaan 3.2.2022. Kaikki voimassaolon päättymishetkellä jäljellä olevat saldot vähennetään lomatyypistä, ja ne näkyvät lomasaldoissa.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Määritä tarvittava liite lomatyyppiä kohden

> [!NOTE]
> Jos haluat käyttää **Liite pakollinen** -kenttää, sinun on ensin otettava **Määritä lomapyyntöjen pakollinen liite** -ominaisuus käyttöön ominaisuuksien hallinnassa. Lisätietoja ominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

1. Valitse **Loma ja poissaolo** -sivun **Linkit**-välilehden **Asetukset**-kohdassa **Loma- ja poissaolotyypit**.

2. Valitse **loma- ja poissaolotyyppi** luettelosta. Määritä **Yleiset**-osassa **Liite pakollinen** -kenttää käyttämällä, onko liite ladattava, kun työntekijä lähettää uuden lomapyynnön valittua lomatyyppiä käyttäen. 

Työntekijöiden on ladattava liite, kun he lähettävät uuden lomapyynnön, jonka lomatyypissä **Liite pakollinen** -kenttä on käytössä. Lomapyynnön hyväksyjät voivat käyttää määritettyjen työnimikkeiden **Liitteet**-vaihtoehtoa tarkastellakseen liitettä, joka on ladattu lomapyynnön osana. Jos lomapyyntöä käytetään Human Resources -sovelluksesta Microsoft Teamsissä, **Näyttötiedot**-valintaa lomapyynnössä voidaan käyttää sen tietojen ja mahdollisten liitteiden tarkasteluun.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Määritä lomayksiköt (päivät/tunnit) lomatyypin mukaan

> [!NOTE]
> Jos haluat käyttää lomayksiköitä lomatyyppiä kohden -toimintoa, sinun on ensin otettava käyttöön **Määritä lomayksiköt lomatyyppiä kohden** -ominaisuus ominaisuuksien hallinnassa. Lisätietoja ominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

> [!IMPORTANT]
> Oletusarvon mukaan yrityksen lomatyypit käyttävät lomayksiköitä yritystason lomaparametrien konfiguraatiosta.
> 
> Loma- ja poissaolotyypin lomayksikköä voi muokata vain, jos lomatyypille ei ole lomatapahtumia.
> 
> Kun toiminto on otettu käyttöön, sitä ei voi poistaa käytöstä.

1. Valitse **Loma ja poissaolo** -sivun **Linkit**-välilehden **Asetukset**-kohdassa **Loma- ja poissaolotyypit**.

2. Valitse loma- ja poissaolotyyppi luettelosta. Valitse sitten **Yleiset**-osan **Yksikkö**-kentästä lomayksikkö. Voit valita **Tunnit** tai **Päivät**.

3. Valinnainen: Jos valitsit **Tunnit** **Yksikkö**-kentässä , voit määrittää **Ota käyttöön puolipäivämääritys** -kentän avulla, voivatko työntekijät valita ensimmäisen puolipäiväisen vai toisen puolipäiväisen vapaapäivän, jos he pyytävät puolen päivän lomaa.

Työntekijät, jotka lähettävät uuden lomapyynnön, voivat muodostaa lomapyyntönsä valitsemalla eri lomatyyppejä. Kaikilla yksittäisen lomapyynnön osana valituilla lomatyypeillä on kuitenkin oltava sama lomayksikkö. Työntekijät voivat tarkastella kunkin lomatyypin lomayksikköä **Pyydä vapaa-aikaa** -lomakkeessa.

## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)
- [Loma- ja poissaolosuunnitelman luominen](hr-leave-and-absence-plans.md)
- [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)
- [Loman keskeyttäminen](hr-leave-and-absence-suspend-leave.md)
- [Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

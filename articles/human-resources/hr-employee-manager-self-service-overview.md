---
title: Työntekijän ja esimiehen itsepalvelun yleiskatsaus
description: Tässä artikkelissa on työntekijän ja esimiehen itsepalvelun työtilan yleiskuvaus.
author: twheeloc
ms.date: 08/26/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a356aae6590c2bce289c8d180324027efc76983
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7992042"
---
# <a name="employee-and-manager-self-service-overview"></a>Työntekijän ja esimiehen itsepalvelun yleiskatsaus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa on työntekijän ja esimiehen itsepalvelun työtilan yleiskuvaus.

## <a name="edit-personal-details"></a>Muokkaa henkilökohtaisia tietoja

Jos haluat lisätä tai muuttaa henkilökohtaisia tietoja, katso [henkilökohtaisten tietojen muokkaaminen](hr-employee-manager-self-service-edit-personal-information.md).

## <a name="user-not-assigned-to-a-worker-record"></a>Käyttäjää ei ole määritetty työntekijätietueeseen

Jos et ole linkittänyt käyttäjää **Työntekijä**-tietueeseen **Käyttäjät**-sivulla, näkyviin tulee seuraava sanoma:

**Käyttäjätunnustasi ei ole liitetty työntekijätietueeseesi järjestelmässä. Et voi katsella tai päivittää tietojasi, ennen kuin tunnus on liitetty. Ota yhteyttä esimieheesi tai tukitiimiin lisäohjeita varten.**

Voit liittää käyttäjän **Työntekijä**-tietueeseen siirtymällä **Käyttäjät**-kohtaan ja valitsemalla käyttäjän. Valitse **Muokkaa**, lisää vastaava työntekijä sivun **Henkilö**-kenttään ja valitse sitten **Tallenna**. **Työntekijän itsepalvelun** käytön pitäisi olla nyt mahdollista.

## <a name="security-requirements-for-employee-and-manager-self-service"></a>Työntekijän ja esimiehen itsepalvelun suojausvaatimukset

Työntekijän ja esimiehen itsepalvelu edellyttää kahta käyttöoikeusroolia:

- Työntekijät tarvitsevat työntekijän roolin.
- Esimiehet tarvitsevat sekä työntekijän että esimiehen roolin.

>[!NOTE]
>Voit käyttää työntekijän ja esimiehen itsepalvelua myös mukautetuilla rooleilla, kunhan niille on annettu Työntekijä- ja Esimies-työtilojen käyttöoikeus.<br>
>Esimiehen työntekijän tietojen käyttöoikeus perustuu Human Resourcesissa tällä hetkellä määritettynä olevaan toimen rivihierarkiaan.

## <a name="employee-self-service"></a>Työntekijän itsepalvelu

**Omat tiedot**-välilehdessä näkyvät seuraavat **työntekijän itsepalvelun** tiedot.  

### <a name="summary"></a>Yhteenveto

**Minulle määritetyt työnimikkeet** näyttää kaikki työntekijälle määritetyt hyväksynnät ja työnkulkunimikkeet. Voit määrittää työnkulun kohteita lähettämään sähköposteja käyttäjälle.

**Minulle osoitetut kyselylomakkeet** näyttävät kaikki suoraan työntekijälle tai ryhmälle osoitetut ajoitetut kyselylomakkeet.

**Yrityshakemiston** avulla työntekijät voivat etsiä organisaation henkilöihin liittyviä tietoja. Julkiset yhteystiedot ovat kaikkien työntekijöiden käytettävissä. Yrityksen hakemisto on rajoitettu yritykseen, johon työntekijä on kirjautunut.

**Ryhmän kalenterissa** näkyvät ryhmän kalenteritiedot. Lisätietoja on kohdassa [Ryhmä- ja yrityskalenterien tarkasteleminen](hr-employee-self-service-calendar.md).

### <a name="my-career-information"></a>Oman uran tiedot

**Työntekijän itsepalvelun** **Omat uratiedot** -osiossa näkyy vapaata ja poissaoloa, suorituskyvyn hallintaa, osaamisalueita, etuja, tehtäviä ja liitteitä koskevia ruutuja.

**Jäljellä olevat saldot** -ruutu näyttää kaikkien rekisteröityjen suunnitelmien saldot. Tämä ruutu ennustaa saldosi perustuen kertymismenetelmään. Voit määrittää ja lähettää aikapyyntöjä, jotka käyvät läpi hyväksynnän työnkulkuprosessin. Lisätietoja lomista ja poissaoloista on kohdassa [Lomien ja poissaolojen yleiskatsaus](hr-leave-and-absence-overview.md).

**Tehtävät**-ruudussa näkyvät tehtävät, jotka on määritetty sinulle ja jonka avulla voit tarkastella ja hallita niitä.

**Seuraava rekisteröity kurssi** näyttää seuraavan kurssin, jolle olet rekisteröitynyt. Voit tarkastella tietoja ja rekisteröityä mille tahansa avoimille kursseille. Kaikkien rekisteröitymiseen avointen kurssien tilana on **Aloitettu**, ja työntekijät voivat rekisteröityä itse. Organisaation asetuksista riippuen kurssin rekisteröinnissä saattaa olla hyväksymisprosessi.

**Varmenteet**-ruudussa näkyy nykyistä päivämäärää lähimpänä olevan sertifikaatin voimassaoloaika ja vanhentumispäivämäärä. Voit päivittää, lisätä tai poistaa sertifikaatteja. Organisaation asetuksista riippuen todistuspäivityksissä saattaa olla hyväksymisprosessi.

**Seuraava ajoitettu tarkistus** näyttää seuraavan suorituskykytarkistuksen. Voit aloittaa uuden arvostelun tästä ruudusta. Esimies tai HR-edustaja voi myös aloittaa arvion. Organisaation asetuksista riippuen saatat myös pystyä tarkastelemaan, päivittämään ja lähettämään poistumisarvosteluja.

Voit hallita tavoitteitasi **Suorituskykytavoite**-ruudulla. Tässä ruudussa näkyy kunkin tilan tavoitteiden määrä **(Ei aloitettu**, **Aikataulussa** ja **Vaatii parannusta**). Voit luoda, päivittää ja poistaa tavoitteita roolipohjaisen suojauksen mukaan. Voit halutessasi lisätä uusia tavoitteita ryhmistä tai malleista. Esimiehet ja HR voivat myös luoda tavoitteita työntekijöiden puolesta ja määrittää, miten yksityiskohtainen kukin tavoite on. Esimiehet ja työntekijät voivat tehdä tavoitteita ja päivittää tehtäviä, mittauksia ja tilaa. Voit myös sisällyttää liitteitä.

Voit tarkastella **Koko osaaminen**-ruudussa olevia osaamisalueita. Voit päivittää osaamisalueita, lisätä uusia tai poistaa niitä, jotka eivät ole enää olennaisia. Organisaation asetuksista riippuen, muutokset osaamisessasi saattavat vaatia hyväksymisprosessin.

Voit tarkastella nykyistä kompensaatiotasi **Kompensaatio**-ruudussa. Valitse **Näytä**, jos haluat nähdä vuosittaisen palkan ja viimeisen korotusmäärän. Jos olet töissä useammassa kuin yhdessä yrityksessä, jokainen vuosittainen summa näkyy. Jos haluat tarkastella yksityiskohtaista kompensaatiohistoriaasi, valitse **Vuosittainen palkkasumma**, joka avaa **Vakio- ja muuttuva kompensaatiohistoria** -sivun. Tuleva kompensaatio ei näy tällä sivulla. Jos sinulla on useita töitä, voit siirtyä tämän sivun yrityksistä toiseen ja tarkastella kompensaatiohistoriaasi kirjautumatta jokaiseen yritykseen.

Tarkastele ja hallitse tiedostoja, joissa on **Liite**-ruutu. Voit hallita kaikkia **Ulkoisia** liitteitä. Sekä HR että työntekijät voivat lisätä liitteitä **työntekijän itsepalvelun** tai **Työntekijä**-sivun avulla. Liitteet asetetaan oletusarvoisesti **Ulkoinen**-tilaan.

### <a name="additional-information"></a>Lisätiedot

Tässä osassa on linkkejä muihin **työntekijöiden itsepalvelu** -alueisiin, jotka muistuttavat **Uratietoni**-osiota.

Voit rekisteröityä etuuksiksi **Edut**-linkin kautta. Lisätietoja etujen hallinnasta on kohdassa [Etujen yleiskuvaus](hr-benefits-management-overview.md).

**Suorituskyky**-kohdassa voit valita **Suorituskykykirjauskansio** luodaksesi suorituskykykirjauskansiomerkintöjä, joita voi käyttää sekä suorituskykytavoitteissa että -arvoisissa. Voit antaa palautetta organisaatiosi muille työntekijöille valitsemalla **Lähetä palaute**. Organisaation asetuksista riippuen sähköpostit voidaan lähettää vastaanottajalle, lähettäjälle ja esimiehille. Voit lähettää palautetta organisaation kaikille työntekijöille. Yritys ei rajoita palautteen lähettämistä.

**Osaamisalueet**-kohdassa voit tehdä muutoksia **Kursseihin**, **Koulutukseen**, **Luottamustoimiin** ja **Ammattikokemukseen**. Organisaation asetuksista riippuen osaamisen päivityksissä saattaa olla hyväksymisprosessi.

Voit tarkastella työn tietoja **Organisaation** alla. Työn tietoihin sisältyvät taidot, todistukset ja vastuualueet ensisijaisesta toimestasi. Voit myös tarkistaa, mitkä lainatut laitteet on kuitattu ulos sinulle. Organisaation asetuksista riippuen, muutokset lainatuissa laitteissa saattavat vaatia hyväksymisprosessin.

**Kyselylomakkeessa** näkyvät valmiit kyselylomakkeet. Voit myös tarkastella koko yrityksen laajuisia kyselylomakkeita, joita ei ole vielä täytetty. Voit halutessasi täyttää kyselylomakkeen milloin tahansa. Kyselylomakkeen laatija voi määrittää aikakehyksen, jota kyselylomake koskee.

Voit määrittää käyttäjän määrittämiä linkkejä **Henkilöstöhallinnon parametreihin**. Voit esimerkiksi määrittää linkit maksulausekkeisiin, vuoden lopun dokumentaatioon tai ulkoisiin ratkaisuihin. Nämä linkit näkyvät tämän osan alaosassa, mutta voit siirtää niitä käyttämällä mukauttamista.

Voit myös luoda uusia välilehtiä upottamalla Power Appsin **työntekijän itsepalvelu** -työtilaan. **Asetukset**-valikon avulla voit mukauttaa sivun millä tahansa Power Appsilla. **Asetukset**-valikossa voit halutessasi lisätä Power Appin, viimeistellä tiedot ja lisätä sovelluksen. Power Apps näkyy oletusarvon mukaan järjestyksessä ensimmäisenä välilehtenä. Voit muuttaa järjestystä käyttämällä normaalia mukauttamista.

## <a name="my-team"></a>Oma ryhmä

**Oma ryhmä** -välilehdessä näkyvät seuraavat **esimiehen itsepalvelun** tiedot. Vain esimiehet voivat käyttää **Oma ryhmä** -välilehteä.

### <a name="personnel-actions"></a>Henkilöstötoiminnot

Henkilöstötoiminnot näkyvät **Henkilöresurssien jaettujen parametrien** ja **Henkilöstöhallinnon parametrien** määritysvaihtoehtojen mukaan. Kun **Työntekijät** ovat käytössä, henkilöstötoiminnot mahdollistavat uudet valikkovaihtoehdot, kuten:

- **Pyydä uutta työntekijää**
- **Pyydä uusi alihankkija**
- **Pyydä työntekijälle uutta toimeksiantoa**
- **Pyydä irtisanomista**
- **Pyydä kompensaation muutosta**

Voit määrittää nämä asetukset ja käydä läpi valinnaisen tarkistus- ja hyväksyntätyönkulun.

**Toimen toiminnon** käyttöönotto mahdollistaa seuraavat vaihtoehdot:

- **Pyydä uutta toimea**
- **Pyydä muutosta toimen tietoihin**

Voit myös määrittää nämä asetukset ja käydä läpi valinnaisen tarkistus- ja hyväksyntätyönkulun.

### <a name="summary"></a>Yhteenveto

**Yhteenveto**-osan tiedot määräytyvät sen mukaan, mitä vaihtoehtoja HR on valinnut **Henkilöstöhallinnon parametreissa**. **Henkilöstöhallinnon parametrit** -sivun **Esimiehen itsepalvelu**-välilehdessä voit määrittää asetukset vanhentuvien tietojen ja avoimien toimien näyttämisestä. Näiden asetusten ottaminen käyttöön määrittää, mitä esimiehet näkevät **Yhteenveto**-osassa.

Voit määrittää seuraavat ruudut esimiehille:

- **Tiimilleni vanhentuviksi määritetyt varmenteet**
- **Ryhmäni vanhentuvat tunnusnumerot**
- **Ryhmäni vanhentuvat koeajat**
- **Ryhmäni vanhentuvat seulonnat**
- **Ryhmäni vanhentuvat testit**
- **Suora ja/tai laajennettuja raportteja koskevat Avoimet toimet**
- **Odottavat lomapyynnöt ryhmäni pyynnöissä**
- **Ryhmän osaamisalueiden arviointi**
- **Osaamisalueanalyysi**
- **Ryhmän suoritustason kirjauskansiot**
- **Tiimin suorituskykytavoitteet**
- **Ryhmän suoritustasoarvioinnit**
- **Lopettavat työntekijät**

Voit määrittää seuraavat asetukset, joiden avulla esimiehet voivat tehdä muutoksia tai lisätä lomapyyntöjä suorien raporttiensa puolesta:

- Varmenteet
- Kurssit
- Lainan kohteet
- Osaamisalueet
- Loma- ja poissaolopyynnöt

### <a name="my-team-information"></a>Oman ryhmän tiedot

**Oma ryhmä** -ruudun avulla esimiehet voivat tarkastella ja päivittää suoria ja laajennettuja raportteja. Jos haluat käyttää laajennettuja raportteja, valitse työntekijä, joka ohjaa ja valitse sitten ruudussa **Näytä ryhmä**. Kaikki samat asetukset koskevat laajennettuja raportteja kuin suoria raportteja. 

#### <a name="summary-tab"></a>Yhteenveto-välilehti

**Yhteenveto**-välilehden avulla voit tarkastella suoria raportteja nopeasti. Jos suora raportti sisältää myös työntekijöitä, jotka raportoivat heille, kortissa näkyy yläosassa olevien suorien raporttien määrä sekä **Näytä ryhmä** -painike. Kunkin ruudun yläpuolella olevat vaihtoehdot koskevat valittua työntekijää. Jos esimerkiksi haluat määrittää lomapyynnön työntekijän puolesta, valitse työntekijä ja valitse sitten **Lomapyyntö**. 

Jos valitset **Tiedot**-painikkeen työntekijän valitsemisen jälkeen, näyttöön tulevat seuraavat asetukset:

- **Varmenteet**
- **Kompensaatio**
- **Kurssit**
- **Arvioinnit**
- **poissaoloaika**
- **Lainatut nimikkeet**
- **Suoritustasotavoitteet**
- **Rekisteröidyt kurssit**
- **Osaamisalueet**
- **Lähetä palaute**

Organisaation asetuksista riippuen voit joko tehdä muutoksia tai vain tarkastella.

#### <a name="position-tab"></a>Toimi-välilehti

**Toimi**-välilehdessä on yhteenvetonäkymä työntekijöistä niiden ensisijaisessa sijainnissa. Kunkin ruudun otsikkoalueella näkyy nimi, ruutu ja osasto. Tämä ruutu sisältää seuraavaa:

- **Ikälisäpäivä** – Näytetään **Työntekijä**-sivun työntekijän yhteenveto-osiosta.
- **Huoltovuodet** – Laskettu työntekijän työsuhteen alkamispäivämäärän perusteella.
- **Aiempien toimien määrä** – Sijaintihistorian perusteella tämän numeron valitseminen avaa kaikkien aiemmin pidossa olevien toimien yksityiskohtaisen näkymän.
- **Syntymäaika** – Työntekijän syntymäpäivän kuukausi ja päivä.

Voit tarkastella sekä suorien että laajennettujen raporttien toimitietoja.

#### <a name="compensation-tab"></a>Kompensaatiovälilehti

**Kompensaatio**-välilehdessä näkyy työntekijän vuosipalkka. Yrityksen tunnus näkyy palkan summa -kentässä. Jos työntekijällä on useampi kuin yksi työsuhde ja hän saa maksun useista yrityksistä, työntekijällä on useita kompensaatiosuunnitelmia. Voit tarkastella kaikkia eri yrityksissä olevia kompensaatiosuunnitelmia yrityksiä vaihtamatta ottamalla käyttöön yritystenvälisen kompensaation. Se tehdään valitsemalla **Henkilöstöhallinto > Jaetut parametrit > Lisäkäyttöoikeudet > Ota yritystenvälinen kompensaatio käyttöön**.

Voit tarkastella kompensaatiohistoriaa valitsemalla **Palkan määrä**, joka avaa **Tiedot**-sivun. Vain nykyiset ja historialliset pysyvät ja muuttuvat kompensaatiotiedot näkyvät **Kompensaatio**-sivulla. Jos työntekijällä on useita työsuhteita, kompensaatiohistoriaa voi tarkastella kussakin yrityksessä tai yritystenvälinen kompensaatio voidaan ottaa käyttöön **henkilöstöhallinnan jaetuissa resursseissa**, jolloin kaikki kompensaatiosuunnitelmat ovat näkyvissä.

Voit tarkastella sekä suorien että laajennettujen raporttien kompensaatiotietoja.

#### <a name="leave-and-absence-tab"></a>Loma- ja poissaolovälilehti

**Loma-ja poissaolo** -välilehdessä näkyvät tehtävän työntekijöiden ylimmät saldot. Jos haluat suorittaa toiminnon tai tarkastella täydellistä luetteloa tehtävistä, **Valitse tiedot** ja valitse sitten **Poissaolo**. **Loma**-sivulla voit tarkastella saldot, pyynnöt, hyväksytyn vapaa-ajan ja ennustaa saldot ja auttaa työntekijöitä hallitsemaan aikaa paremmin. Organisaation asetuksista riippuen voit myös pyytää lomaa, joka on käytössä suorissa ja laajennetuissa raporteissa.

#### <a name="performance-goals-tab"></a>Suorituskykytavoitteet-välilehti

**Suorituskykytavoitteet**-välilehdessä on yhteenveto suorituskykytavoitteista tilan mukaan. Valitse tilan numero tai valitse suorituskykytavoitteet **Tiedot**-kohdasta, jos haluat nähdä kaikki työntekijän tavoitteet. Esimiehet ja työntekijät voivat päivittää tavoitteita tarpeen mukaan tavoitteen keston aikana.

Esimiehet voivat nähdä kaikki ryhmänsä tavoitteet **Ryhmän suorituskykytavoitteet** -ruudun avulla **Oman ryhmän** **Yhteenveto**-osassa.

#### <a name="reviews-tab"></a>Arvostelut-välilehti

**Arvostelut**-välilehdessä on yhteenveto työntekijän kussakin tilassa tekemistä tarkastelusta: **keskeneräinen**, **valmis tarkistettavaksi** ja **lopullinen tarkistus**. Voit käyttää työntekijän tarkistusta valitsemalla **Tiedot**-painikkeen ja valitsemalla sitten arvostelut. Kun tarkistus on työnkulkuprosessin sisällä, voit tarkistaa, onko tarkistus käytettävissä päivitystä varten. 

Esimiehet voivat nähdä kaikki ryhmänsä arvostelut **Ryhmän suorituskykyarviot** -ruudun avulla **Oman ryhmän** **Yhteenveto**-osassa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

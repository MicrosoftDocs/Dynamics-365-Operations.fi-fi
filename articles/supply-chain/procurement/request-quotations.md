---
title: Tarjouspyynnöt – yleiskatsaus
description: Tässä artikkelissa on tarjouspyyntöjen yleiskuvaus. Organisaatiot tekevät tarjouspyyntöjä, kun ne haluavat ostaa tarvitsemiaan nimikkeitä tai palveluita ja haluavat saada kilpailukykyisiä tarjouksia useilta toimittajilta.
author: GalynaFedorova
ms.date: 10/05/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2154"
- intro-internal
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89abf82879ab08f2341ce5b14e6af1d5c42140b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895580"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Tarjouspyynnöt – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tarjouspyyntöjen yleiskuvaus. Organisaatiot tekevät tarjouspyyntöjä, kun ne haluavat ostaa tarvitsemiaan nimikkeitä tai palveluita ja haluavat saada kilpailukykyisiä tarjouksia useilta toimittajilta. Tarjouspyynnössä pyydät toimittajilta hinnat ja toimitusaikoja nimikkeiden määrille, jotka määrität.
Voit myös pyytää toimittajia määrittämään, liittyykö tarjoukseen satunnaisia kuluja, esimerkiksi lähetyskustannuksia, tai tarjoaako toimittaja alennuksia suurista tilauksista tai toimittajalaskun maksamisesta aikaisin.

Tarjouspyyntöprosessi muodostuu seuraavista tehtävistä:

1. Tarjouspyynnön luominen ja lähettäminen vähintään yhdelle toimittajalle.
1. Tarjousten (tarjouspyyntövastausten) vastaanottaminen ja rekisteröiminen.
1. Hyväksyttyjen tarjousten siirtäminen ostotilaukseen, ostosopimukseen tai ostoehdotukseen.

Seuraavassa kuvassa on yhteenveto tarjouspyyntöprosessista.

[![Tarjouspyyntöprosessi.](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Voit luoda tarjouspyyntötapauksen suunnitelluista tilauksista, ostoehdotuksesta tai manuaalisesta kirjauksesta. Tarjouspyyntötapaus on perusasiakirja, jonka perusteella tarjouspyyntö tehdään kullekin toimittajalle.

Kun olet valmistellut tarjouspyyntötapauksen ja lisännyt toimittajat, valitse tarjouspyyntötapauksessa **Lähetä** (**Lähetä ja julkaise** julkisella sektorilla). Tarjouspyynnön kirjauskansio luodaan jokaiselle toimittajalle, jolle lähetät tarjouspyynnön. Voit määrittää Lähetä-toiminnon tulostusasetukset joko tulostamaan raportin jokaisesta toimittajasta arkistoon vai lähettämään raportin kunkin toimittajan sähköpostiosoitteeseen. Voit lisäksi luoda kunkin toimittajan tarjouspyynnön kirjauskansiossa raportin, jonka voit lähettää toimittajalle tai lähettää sen myöhemmin uudelleen. Voit myös määrittää Lähetä-toiminnon luomaan vastauslomakkeen, jonka toimittaja voi täyttää.

Tässä artikkelissa käsitellään tarjouspyyntöjen käsittelyprosessi silloin, kun toimittajayhteistyö ei ole käytössä. Jos järjestelmä on määritetty toimittajayhteistyötä varten, toimittajat voivat antaa tarjouksia suoraan Supply Chain Managementissa. Lisätietoja on kohdassa [Toimittajayhteistyö asiakkaisen kanssa](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) ja [Toimittajayhteistyö ulkoisten toimittajien kanssa](vendor-collaboration-work-external-vendors.md).

Jos tarjouspyyntöä on muutettava lähettämisen jälkeen, voit lähettää tarjouspyynnön uudelleen toimittajille, kun olet käyttänyt kahta muutostoimintoa: luontia ja viimeistelyä.

Sähköpostitse vastaanotettavat tarjoukset voidaan käsitellä **Tarjouspyynnöt**-sivulla.

Jos tietyltä toimittajalta tarvitaan vastauksen toinen iteraatio, valitse **Tarjouspyyntö**-sivulla **Palauta**. Palautustoiminto luo uuden kirjauskansion ja raportin, joka tulostetaan, arkistoidaan ja lähetetään tulostusasetusten mukaisesti.

Jos olet lisännyt tarjouspyyntötapahtumaan pisteytysehtoja, tarjouspyynnössä on pisteytyspaneeli, johon voit lisätä pisteet. Kokonaispisteytys näkyy tarjouspyynnössä ja vertailtaessa vastauksia **Vertaa vastauksia** -sivulla. Voit verrata **Vertaa vastauksia** -sivulla myös muita vastaustietoja, kuten rivihintaa, toimituspäivämäärää ja kokonaishintaa.

Kun olet valinnut tarjouksen tai tarjouksen rivejä, voit hyväksyä kaikki rivit tai osan riveistä ja hylätä loput. Luotavat hyväksymiskirjauskansiot, hylkäämiskirjauskansiot ja vastaavat raportit tulostetaan, arkistoidaan ja lähetetään tulostusasetusten mukaisesti. Kun hyväksyt tarjouksen tai tietyt tarjouksen rivit, järjestelmä luo joko ostosopimuksen tai ostotilauksen tai päivittää ostoehdotuksen tarjouspyynnön ostotyypin mukaan. Voit luoda haluamistasi vastauksista kauppasopimuksen käytettäväksi myöhemmin huolimatta siitä, oletko hyväksynyt tai hylännyt kyseiset vastaukset.

Tarjouspyyntötapauksessa on kaksi tilaa: alin ja ylin. Voit tarkastella tilaa **Kaikki tarjouspyynnöt** -luettelosivulla. Alin tila on minkä tahansa tarjouspyyntötapauksen rivin vähiten edistynyt vaihe, ja korkein tila on minkä tahansa tarjouspyyntötapauksen rivin kaikkein edistynein vaihe. Jos esimerkiksi kolmirivinen tarjouspyyntötapaus lähetetään kahdelle toimittajalle, tarjouspyyntöjä on kaksi ja kullakin on kolme riviä. Kaikkien rivien tila on **Lähetetty**. Tarjouspyyntö on nyt annettu jostakin toimittajasta ja tarjouspyynnön rivien tilaksi tulee **Vastaanotettu**. Tämän vuoksi tarjouspyyntötapauksen kaikkien kolmen rivin tila yhdessä tarjouspyynnössä **Lähetty** ja toisessa **Vastaanotettu**. Alin tila on sitten **Lähetetty** ja ylin tila **Vastaanotettu.**

Näitä tiloja käsitellään tarkemmin jäljempänä tässä artikkelissa.

## <a name="setting-up-rfq-functionality"></a>Tarjouspyyntötoimintojen asetukset

Ennen tarjouspyyntötapauksen luomista sinun täytyy määrittää tarjouspyynnön tiedot **Hankintaparametrit**-sivulla. Tarjouspyyntötapausta luodessasi voit määrittää oletusarvot, jotka kopioidaan tarjouspyyntöön. Voit määrittää seuraavat oletusarvot:

- Uusien tarjouspyyntöjen ostotyyppi: **Ostotilaus** tai **Ostosopimus**
- Vanhentumispäivä ja siirtymäaika tarjouspyynnön luontipäivästä.
- Pyyntötyyppi, joka voi liittää tietyn oletuspisteytysmenetelmän tarjouspyyntötapahtumaan.
- Toimitustiedot ja maksuehdot.

Nämä arvot voi ohittaa tietyissä tarjouspyyntötapauksissa.

Myös muutosprosessi täytyy määrittää. Tämän määrityksen yhteydessä voit ottaa käyttöön kentän lukituksen. Kun kentän lukitus on käytössä ja hankinta-asiantuntija haluaa tehdä tarjouspyyntöön muutoksia, hänen on ensin valittava tarjouspyyntötapauksen **Tarjous**-välilehden **Muutos**-osassa **Luo**. Kun tarjouspyyntötapaus on päivitetty muutoksella, hankinta-asiantuntijan on viimeisteltävä prosessi valitsemalla **Viimeistele**. Viimeistelytoiminto luo sähköpostiviestin, joka ilmoittaa toimittajille tarjouspyynnön muutoksesta.

Valitse **Hankintaparametrit**-sivulla toimittajille lähetettävän sähköposti-ilmoituksen malli. Kun malli luodaan **sähköpostimalleissa**, se voi sisältää seuraavia korvaavia tunnisteita:

- %Tarjouspyyntötapaus%
- %Tarjouksen palautuksen syy%
- %Muutoksen syy%
- %Muutoksen valmistelija%
- %Company%
- %Tarjouspyyntötapauksen nimi%
- %Ajon vanhenemispäivä%
- %Date%

%Tarjouksen palautuksen syy%- ja %Muutoksen syy% -tunnisteet korvataan tekstillä, jonka hankinta-asiantuntija voi täyttää viimeistellessään muutoksia ohjatussa **Muutos**-toiminnossa. %Muutoksen valmistelija%- ja %Company%-tunnisteet korvataan automaattisesti tarjouspyynnön tiedoilla. %Date%-tunniste korvataan nykyisellä päivämäärällä.

Jos haluat peruuttaa tarjouspyynnön lähettämisen jälkeen, se voidaan tehdä tarjouspyyntötapauksessa. Peruutusta varten tarvitaan sähköpostimalli lähettämään peruutusilmoitus toimittajan yhteyshenkilöille. Malli on oltava valittuna **Hankintaparametrit**-sivulla. Luotava malli voi sisältää seuraavat korvattavat tunnisteet:

- %Peruutuksen syy%
- %Tarjouspyyntötapaus%
- %Tarjouspyynnön peruuttaja%
- %Company%
- %Tarjouspyyntötapauksen nimi%
- %Date%

%Peruutuksen syy% -tunniste korvataan tekstillä, jonka hankinta-asiantuntija voi antaa ohjatussa **Peruutus**-toiminnossa. %Date%-tunniste korvataan nykyisellä päivämäärällä.

Jos haluat osoittaa tarjouksessa tarjouksen hylkäämisen tai hyväksymisen syyn syykoodeilla, määritä syykoodit **Toimittajan syyt** -sivulla.

Voit määrittää hankinnan **Lomakeasetukset**-sivulla tulostettujen tai tallennettujen tarjouspyyntöasiakirjojen ulkoasun.

> [!NOTE]
> Julkisen sektorin määrityksessä jo lähetettyyn tarjouspyyntöön tehdyt muutokset edellyttävät muutosprosessin käyttöä. Kun tarjouspyyntö on lähetetty, kentät lukitaan.
Niinpä tarjouspyyntöön tehtävät muutokset edellyttävät edellä kuvatun muutosprosessin aloittamista valitsemalla **Luo**. Lukitustoimintaa ohjataan **Hankintaparametrit**-sivun **Lukitse tarjouspyynnöt, kun ne on lähetetty** -asetuksella. Parametrin arvoksi määritetään oletusarvoisesti **Kyllä**. Julkisen sektorin määrityksissä tämä on oletusasetus, jota ei voi muuttaa. Vaikka muutosprosessia voidaankin käsitellä manuaalisesti muissa kuin julkisen sektorin määrityksissä, sitä on käytettävä julkisen sektorin määrityksissä.

Kun luot ostotilaustyyppisen tarjouspyyntötapauksen ja lisäät tarjouspyyntöön varastonimikkeen, luotavan varastotapahtuman vastaanoton tila on **Tarjouksen vastaanotto**. Vain tarjouspyyntötapauksen rivit, joilla on tämä tila, otetaan huomioon, kun lasket toimituksia pääsuunnitelmaa käyttämällä. Jos haluat, että pääsuunnitelma sisältää tarjouspyyntötapauksen rivejä odotettuna vastaanottona, se on määritettävä pääsuunnittelun asetuksissa.

Ostopäällikkö tai edustaja voi luoda ja ylläpitää pyyntötyyppejä, jotka vastaavat organisaation hankintavaatimuksia. Kukin pyyntötyyppi voidaan liittää pisteytystapaan. Pisteytysmenetelmät koostuvat ehdoista, joita voi käyttää tarjouksia pisteytettäessä. Pyyntötyypit, pisteytysmenetelmät ja pisteytysehdot määritellään **Pyyntötyyppi**- ja **Pisteytystapa**-sivuilla.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Toimittajan tarjouspyynnön vastauslomakkeisiin sisällytettävät oletuskentät

Voit määrittää toimittajilta tarjouspyyntöjen vastauksissa (tarjouksissa) saatavien tietojen tyypin. Oletuksiksi määritetyt kentät sisällytetään toimittajan yhteistyötä varten annettuun verkkolomakkeeseen. Määritä asetukset seuraavasti:

1. Jos et ole vielä tehnyt niin, ota *Valitse toimittajan tarjouspyynnön vastauslomakkeisiin sisällytettävät tarjouspyyntökentät* -ominaisuus käyttöön [Ominaisuuden hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa.
1. Valitse **Hankinta > Asetukset > Hankintaparametrit**.
1. Avaa **Tarjouspyyntö**-välilehti.
1. Valitse **Oletustarjouspyyntö**-vastauskentän linkki **Tarjouspyyntöjen oletusarvojen määrittäminen** -otsikon alta.
1. **Oletustarjouspyynnön vastauskentät** -valintaikkuna avautuu.
1. **Toimittajan tarjouspyynnön vastauslomakkeisiin sisällytettävät tarjouspyyntölomakkeet** -osassa jokaisen tarjouspyynnön vastauslomakkeessa käytettävissä olevan kentän kohdalla on liukusäädin. Ne kentät, joiden asetuksena tässä osassa on *Kyllä*, sisällytetään (arvoineen) tarjouspyynnön vastauslomakkeissa. Määritä liukusäädin *Ei*-asentoon kunkin sellainen kentän osalta, joita et halua toimittajien näkevän töitä tarkasteltaessa. Tällä tavoin tarjouspyyntötapahtuman aikana voidaan antaa arvioituja tai odotettavia arvoja sisäistä käyttöä varten ilman, että toimittaja näkee, mitä on annettu.

Voit ohittaa nämä asetukset tarvittaessa yksittäisten tarjouspyyntötapahtumien kohdalla.

## <a name="creating-and-sending-an-rfq"></a>Tarjouspyynnön luominen ja lähettäminen

Voit luoda tarjouspyyntötapauksen ja valita toimittajat, joiden haluat lähettävän tarjouksia, ja lähettää sitten tarjouspyynnöt toimittajille. Voit lähettää tarjouspyyntöraportin ja vastauslomakeraportit tulostusasetusten avulla ensisijaiseen sijaintiisi.

Voit luoda tarjouspyyntötapauksen manuaalisesti joko **Ostotilaus**- tai **Ostosopimus**-ostotyypeille.

Jos tarjouspyyntötapauksen tyyppi on **Ostotilaus**, toiminta eroaa seuraavasti muista tarjouspyyntötapausten tyypeistä:

- Kun tarjouspyyntötapauksen rivejä luodaan, järjestelmä luo varastotapahtumia, joiden vastaanottotila on **Tarjouksen vastaanotto**.
- Kun hyväksyt tarjouksen, ostotilaus luodaan.

Jos tarjouspyynnön tyyppi on **Ostosopimus**, toiminta eroaa seuraavasti muista tarjouspyyntötapauksista:

- Tarjouspyyntötapausta käytetään sopimuksessa, kun tuotetta halutaan ostaa tietty määrä tai arvo tiettynä aikana. Valitse tällöin ostosopimusta koskeva päivämääräalue ja ostosopimusta hallinnoivan henkilön nimi.
- Kun hyväksyt tarjouksen, ostosopimus luodaan.

Jos tarjouspyyntötapahtuma luodaan ostoehdotuksesta, **Ostoehdotus**-tyyppi määritetään automaattisesti. Tarjouspyyntötapausta, jonka tyyppi on **Ostoehdotus**, ei voi luoda manuaalisesti.

Voit luoda tarjouspyyntötapauksen ostoehdotuksesta vain, jos ostoehdotuksen tila on **Tarkistuksessa** ja sinut on määritetty suorittamaan seuraava työnkulkutehtävä. Ostoehdotuksen rivit päivittyvät automaattisesti, kun hyväksyt toimittajilta saamiasi tarjouksia (tarjouspyynnön vastauksia). Et voi viimeistellä, hylätä, hyväksyä tai suorittaa muita toimenpiteitä ostoehdotuksessa, ennen kuin ehdotusrivi on päivitetty hyväksytyllä tarjouspyynnön rivillä tai tarjouspyyntötapaus on peruutettu.

Kun luot tarjouspyyntötapauksen, voit valita pyyntötyypin. Pyyntötyyppi määrittää pisteytysehdot, joilla tarjouspyynnön vastauksia pisteytetään tarjouspyyntötapaukseen.

Voit lisätä tarjouspyyntötapaukseen kyselylomakkeen. Kyselylomake näkyy tämän jälkeen kaikissa tarjouspyynnön vastauksissa, kun tarjouspyyntö on lähetetty. Kyselylomakkeen täyttäminen on pakollinen ennen tarjouksen lähettämistä tehtävä tehtävä.

Vaikka oletusarvot annetaan, voit muuttaa tarvittaessa **Toimittajan tarjouspyynnön vastauslomakkeisiin sisällytettävät tarjouspyyntölomakkeet** -asetuksia yksittäisen tarjouspyyntötapahtuman osalta. Sen voi tehdä luomalla tai avaamalla tarjouspyyntötapahtuman. Avaa sitten toimintoruudussa **Tarjous**-välilehti ja valitse **Vastaukset**-osassa **Määritä tarjouspyynnön vastauksen oletusarvot**. **Oletustarjouspyynnön vastauskentät** -valintaikkuna avautuu. Se toimii samalla tavoin kuin määritettäessä toimittajan tarjouspyynnön vastauslomakkeiden oletusarvoja, joskin tässä tehdyt muutokset vaikuttavat vain nykyiseen tarjouspyyntötapaukseen. Lisätietoja tämän toiminnon käyttöönottamisesta ja sen käyttämisestä on kohdassa [Toimittajan tarjouspyynnön vastauslomakkeisiin sisällytettävät oletuskentät](#default-reply-fields).

Tarjouspyyntötapahtumaan lisättäviä toimittajia voi valita kolmella tavalla:

- Voit lisätä toimittajia yksitellen.
- Voit hakea kaikkia toimittajia, jotka täyttävät tietyt ehdot.
- Voit lisätä automaattisesti kaikki toimittajat, jotka on hyväksytty tarjouspyyntötapahtuman riveillä käytettyihin hankintaluokkiin.

Kun tarjouspyyntötapaus on valmis, valitse **Lähetä**. Lähetystoiminto luo kirjauskansiot ja raportit, jotka tulostetaan, arkistoidaan ja lähetetään tulostusasetusten mukaisesti.

Jos valitset **Käytä toimittajaa hintojen uudelleenlaskemiseen**- ja **Käytä toimittajakohtaisia nimiketietoja** -asetukseksi **Kyllä** **Lähetetään tarjouspyyntöä** -sivulla, kun lähetät tarjouspyynnön toimittajalle, jotkin toimittajakohtaiset tiedot täytetään automaattisesti kyseisen toimittajan tarjouspyynnössä.

## <a name="amending-an-rfq-case"></a>Tarjouspyyntötapahtuman muuttaminen

Tarjouspyyntötapahtuman voi joutua muuttamaan vielä senkin jälkeen, kun se on lähetetty. Tarjouspyyntötapahtumaa on ehkä muutettava siksi, että toimituspäivämäärät ovat muuttuneet tai tuotteita tarvitaan lisää tai eri määrinä. Voit määrittää muutosprosessin rajoittavammaksi tai joustavammaksi.

Jos määrität muutosprosessin rajoittavammaksi, aloita muutos valitsemalla tarjouspyyntötapauksessa **Luo** ennen lähetetyn tarjouspyyntötapauksen kenttien muokkaamista. Kun olet tehnyt haluamasi muutokset, valitse **Viimeistele**. Tämän jälkeen saat ohjeet tietojen lisäämisestä sähköpostiviestiin, jolla muutoksesta ilmoitetaan toimittajille. Viestiin liitetään automaattisesti päivitetty tarjouspyyntöraportti, jossa on muutosta koskeva huomautus.

Jos määrität joustavan muutosprosessin, sinun ei tarvitse valita **Luo** ennen jo lähetetyn tarjouspyyntötapauksen kenttien muokkaamista. Muutoshuomautus on kuitenkin lisättävä tarjouspyyntöön manuaalisesti ja tapaus on lähetettävä uudelleen. Huomaa, että tätä menettelyä voi käyttää vain, jos yhtäkään vastausta (tarjousta) ei ole muokattu. Jos olet kirjannut vastauksen ja sen tila on **Vastaanotettu**, **Lähetä**-painike ei ole käytettävissä. Siinä tapauksessa sinun on valittava ensin **Luo** ja sitten **Viimeistele** samoin kuin rajoittavassa prosessissa. Vastaus palautetaan sitten vastaamaan tarjouspyyntötapauksen muutoksia.

Jos toimittajat kirjaavat tarjoukset toimittajayhteistyöliittymässä, sinun on ilmoitettava tarjouspyyntötapauksen muutokset käyttämällä muutosprosessia. Tämä prosessi auttaa estämään tilanteen, jossa toimittajat tekevät tarjouksen vanhentuneesta tarjouspyynnöstä, kun heidän tarjouksensa on kesken. Lisätietoja siitä toimittajayhteistyöstä on kohdassa [Toimittajayhteistyö ulkoisten toimittajien kanssa](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Jos haluat kutsua tarjouksia muilta toimittajilta eikä tarjouspyyntötapaukseen ole tehty muutoksia, voit käyttää **Lähetä**-painiketta. Lisäämäsi toimittajat näkyvät **Lähetä**-sivulla, ja he vastaanottavat sähköpostikutsun.

## <a name="receiving-and-registering-rfq-replies"></a>Tarjouspyyntövastausten vastaanottaminen ja rekisteröiminen

Kun lähetät tarjouspyynnön, ohjelma luo automaattisesti vastauslomakkeen. Kun vastaanotat tarjouspyynnön tarjouksia, sinun on kirjattava ne **Tarjouspyyntö**-sivulla valitsemalla **Muokkaa tarjouspyynnön vastausta** -toimintoa. Voit antaa tällä tavoin tarjouksen tiedot asianmukaisella tarjouslomakkeella. **Vastauksen edistyminen** -tilana on aluksi **Ei aloitettu**. Kun valitset **Muokkaa tarjouspyynnön vastausta** edistymisen tilana on **Ostaja päivittää** siihen saakka, että tarjous lähetetään. Valitse **Lähetä**, kun olet antanut tarjouksen tiedot. Vastauksen edistymisen tilaksi muuttuu **Ostaja on lähettänyt.** Kun toimittajayhteistyö on otettu käyttöön, **Vastauksen edistyminen** päivittyy vastaavasti toimittajan käyttäessä tarjousta. **Toimittaja päivittää** -tila muuttuu sitten tilaksi **Toimittaja on lähettänyt**. Kun tarjous on lähetetty, kirjauskansio luodaan **vastaanotettuna**. Vastaus (tarjous) on lähetettävä, jotta se voidaan rekisteröidä vastaanotetuksi, jonka jälkeen se voidaan käsitellä hyväksytyksi tai hylätyksi.

Jos tarjous on päivitettävä, käytä edellä mainittua prosessia ja lähetä tarjous uudelleen.

Huomaa, että **Tarjouspyyntö**-lomakkeessa voi muokata vain tietoja, jotka liittyvät tarjouksen käsittelyyn. Muokkausta ei siis voi käyttää tarjouksen antamiseen. Voit antaa tai muokata tarjousta valitsemalla **Muokkaa tarjouspyynnön vastausta.**

Jos tarjouspyyntötapahtuma sallii vaihtoehtoiset rivit tarjouksen tietoja annettaessa, voit lisätä vaihtoehtoisia rivejä riveille, joilla on vain hankintaluokka ja joille ei ole määritetty yhtään luettelon nimikettä. Lisää vaihtoehtoisia rivejä valitsemalla **Lisää vaihtoehto**.

Jos olet kirjoittanut vastauksen mutta edellytät toimittajalta uutta tarjousta, voit palauttaa tarjouspyynnön. Luotava uusi kirjauskansio ja raportti voidaan lähettää toimittajalle.

Kaikkien tarjouspyyntöjen ja niiden tilojen (**lähetetty, vastaanotettu, hyväksytty, hylätty, peruutettu, torjuttu**) yhteenveto on nähtävissä **Tarjouspyynnön seuranta** -sivulla.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Tarjousten hyväksyminen ja hylkääminen sekä hyväksyttyjen tarjousten siirtäminen alatason asiakirjoihin

Kun olet löytänyt parhaan tarjouksen, esimerkiksi sellaisen, jonka kokonaishinta on paras, voit hyväksyä sen. Voit hyväksyä joitakin tarjouksen rivejä ja hylätä muut.
Voit myös hyväksyä rivejä eri toimittajilta. Huomaa, että jos hyväksyt joitakin rivejä, sinua pyydetään hylkäämään kaikki muut rivit. Jos siis haluat hyväksyä muitakin rivejä, valitse kysyttäessä **Peruuta**. Kunkin sellaisen toimittajan tarjouspyynnön vastauksen tilaksi, jonka tarjouksia tai rivejä hyväksyt, päivitetään **Hyväksytty**.

Jos sinun on ostotilausta tai ostosopimusta valmisteltaessa lisättävä lisärivi tarjouspyyntöön, voit tehdä sen valitsemalla **Lisää rivi** **Tarjouspyyntö**-sivun riviruudukossa. Voit tarkastella ja muokata tätä riviä vain **Tarjouspyyntö**-sivulla. Se tulee näkyviin tarjoussivulle, kun se on hyväksytty.

Kun hyväksyt tarjouksen tai yhden tarjouksen rivin tai useita rivejä, ostotilaus tai -sopimus luodaan automaattisesti. Voit sitten hylätä muilta toimittajilta saadut tarjoukset.

Voit lisätä vastaukseen syykoodin, joka selittää, miksi tarjous on hyväksytty tai hylätty.

Kun hyväksyt **Ostoehdotus**-tyyppisen tarjouksen, ostoehdotusrivit päivitetään seuraavilla, hyväksytyn tarjouksen tietoja vastaavilla tiedoilla:

- Yksikköhinta
- Alennusprosentti
- Alennuksen suuruus
- Oston kulut
- Rivin kulut
- Toimittaja
- ulkoinen tunnus
- Ulkoinen kuvaus

Seuraavassa taulukossa näkyy, miten tarjouspyynnön tila muuttuu, kun hyväksyt ja hylkäät toimittajien tarjouksia.

## <a name="statuses--highest-and-lowest"></a>Tilat – ylin ja alin

Tarjouspyyntötapauksen Toimittaja-välilehdessä on rivejä, joilla on tietyn toimittajan ylin ja alin tila. Jos toimittajaa lisättäessä ei ole vielä lähetetty rivejä, sekä ylin että alin tila on <strong>Luotu</strong>. Kun toimittajalle lähetettävässä tarjouspyynnössä on kaikki rivit, kahden rivin tilin on <strong>Lähetetty</strong>. Jos jotkin toimittajan tarjouksen rivit hyväksytään ja toiset hylätään, hylätyillä riveillä on alin tila eli <strong>Hylätty</strong>, kun taas hyväksytyillä riveillä on ylin tila eli <strong>Hyväksytty</strong>.

Tarjouspyyntötapauksen riveillä näkyy kaikkien toimittajien rivikohtainen ylin ja alin tila. Jos olet lähettänyt rivin kaikille tarjouspyyntötapauksen toimittajille eikä kukaan ole vielä vastannut, sekä alin että ylin tila on **Lähetetty.** Kun vähintään yksi toimittaja vastaa, ylimmäksi tilaksi tulee **Vastaanotettu**. Jos lisäät uuden toimittajan tapaukseen, alimmaksi tilaksi tulee **Luotu**.

Tarjouspyyntötapauksen ylin ja alin tila on \<Toimittaja- ja Rivit-välilehtien tilakooste.

Tilat asetetaan seuraavaan järjestykseen alimmasta ylimpään: luotu, lähetetty, vastaanotettu, hylätty, hyväksytty, torjuttu, peruutettu.

Seuraavassa taulukossa näkyvät tarjouspyyntötapauksen tilan muutokset, kun luot tarjouspyyntötapauksen, jossa on rivejä, ja lähetät sen sitten toimittajille.

| **Toimenpide**                                | **Alin tarjouspyyntötapauksen tila** | **Ylin tarjouspyyntötapauksen tila** | **Alin tarjouspyyntötapauksen rivin tila** | **Ylin tarjouspyyntötapauksen rivin tila** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Luo tarjouspyyntötapauksen otsikko ja rivi.      | Luotu                    | Luotu                     | Luotu                         | Luotu                          |
| Lähetä tarjouspyynnöt kaikille tarjouspyyntötapauksen kaikille toimittajille. | Lähetetty                       | Lähetetty                        | Lähetetty                            | Lähetetty                             |
| Lisää toinen toimittaja.                       | Luotu                    | Lähetetty                        | Luotu                         | Lähetetty                             |
| Lähetä tarjouspyyntö toiselle toimittajalle.        | Lähetetty                       | Lähetetty                        | Lähetetty                            | Lähetetty                             |

Kaikkien tarjouspyyntötapaukseen liittyvien tarjouspyyntörivien tila on **Lähetetty**.

Seuraavassa taulukossa näkyy, miten tarjouspyynnön tila muuttuu, kun vastaanotat tarjouksia ja rekisteröit tiedot tarjouspyynnön vastauslomakkeeseen.

| **Toimenpide**                                               | **Alin tila kaikkien tarjouspyyntöjen kaikilla riveillä** | **Ylin tila kaikkien tarjouspyyntöjen kaikilla riveillä** | **Alin tarjouspyyntötapauksen otsikon tila** | **Ylin tarjouspyyntötapauksen otsikon tila** | **Alin tarjouspyyntötapauksen rivin tila** | **Ylin tarjouspyyntötapauksen rivin tila** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Rekisteröi yhden toimittajan tarjous tarjouspyyntöön ja tallenna se.        | Lähetetty                                           | Vastaanotettu                                        | Lähetetty                              | Vastaanotettu                           | Lähetetty                            | Vastaanotettu                         |
| Rekisteröi toisen toimittajan tarjous tarjouspyyntöön ja tallenna se. | Vastaanotettu                                       | Vastaanotettu                                        | Vastaanotettu                          | Vastaanotettu                           | Vastaanotettu                        | Vastaanotettu                         |


Seuraavassa esimerkissä on sellaisen tarjouspyyntötapauksen ylin ja alin tila, jossa yksi tarjous on vastaanotettu ja toinen tarjous on hyväksytty. Kun vastaanotettu tarjous hylätään, alin tila muuttuu vastaanotetusta hylätyksi tarjouspyyntötapauksen otsikossa ja rivillä.


|            <strong>Toimenpide</strong>             | <strong>Alin tila kaikkien tarjouspyyntöjen kaikilla riveillä</strong> | <strong>Ylin tila kaikkien tarjouspyyntöjen kaikilla riveillä</strong> | <strong>Alin tarjouspyyntötapauksen otsikon tila</strong> | <strong>Ylin tarjouspyyntötapauksen otsikon tila</strong> | <strong>Alin tarjouspyyntötapauksen rivin tila</strong> | <strong>Ylin tarjouspyyntötapauksen rivin tila</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Hyväksy yksi tarjouksista. (tai vähintään yksi rivi) |                          Vastaanotettu                           |                           Hyv.                           |                    Vastaanotettu                    |                    Hyv.                     |                   Vastaanotettu                   |                   Hyv.                    |
|           Hylkää kaikki muut tarjoukset.           |                          Hylätty                           |                           Hyv.                           |                    Hylätty                    |                    Hyv.                     |                   Hylätty                   |                   Hyväksytty                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: B2B-verkkokauppasivuston määrittäminen
description: Tässä aiheessa kuvataan, kuinka määritetään yritysten (B2B) verkkokauppasivusto Microsoft Dynamics 365 Commercen avulla.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ac6f6511f4f96c00e10369329b2111a46f23d1a2
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035904"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>B2B-verkkokauppasivuston määrittäminen

[!include [banner](../../includes/banner.md)]

Yritysten välisillä (B2B) verkkokauppasivustoilla on joitakin avaintoimintoja, jotka optimoivat B2B-käyttäjän työnkulun. Tässä aiheessa kuvataan, kuinka määritetään B2B-verkkokauppasivusto Microsoft Dynamics 365 Commercen avulla. Se käy läpi moduulit ja sivuston asetukset, jotka pitää olla konfiguroitu B2B-skenaarioiden käyttöön ottamiseksi.

## <a name="prerequisites"></a>Edellytykset

- Jotta voit määrittää B2B-verkkokauppasivuston, tietyt Commerce Headquarters -toiminnot on otettava käyttöön ja määritettävä tässä ohjeaiheessa kuvatulla tavalla.
- Ydinkokemuksia, kuten tuotteiden hakua, tuotetietosivuja, ostoskoria ja uloskuittausta, ylläpitävät samat moduulit, joita käytetään kuluttajakaupan (B2C) verkkokauppasivustoissa. Sivuston laatijoiden tulisi tutustua kaikkiin moduuleihin, joita Dynamics 365 Commerce tukee. Lisätietoja on ohjeaiheessa [Moduulikirjaston yleiskatsaus](../starter-kit-overview.md).
- Tässä aiheessa oletetaan, että sivuston laatijat ymmärtävät perustiedot Commercen sivuston luontitoiminnosta, malleista, katkelmista ja sivuista, jotta he voivat ottaa käyttöön B2B-toiminnot sähköistä kaupankäyntiä varten.

## <a name="site-level-settings"></a>Sivustotason asetukset

Voit käyttää sivustotason asetuksia sivustonmuodostajassa kohdassa **Sivuston asetukset \> Laajennukset**. Seuraavat kaksi sivustotason asetusta koskevat B2B-skenaarioita:

- **Ota käyttöön asiakastilin maksut** – Tämän ominaisuuden avulla käyttäjät voivat maksaa tilauksista asiakastilien avulla. Käytettävissä olevat arvot ovat **Käytössä B2B-asiakkaille**, **Käytössä B2C-asiakkaille**, **Käytössä kaikille asiakkaille** ja **Pois käytöstä kaikilta asiakkailta**. Jos B2B-sivusto tukee asiakastilejä, valitse **Käytössä B2C-asiakkaille**.
- **Ota käyttöön tilausten määrärajat** – Tämän ominaisuuden avulla voit määrittää kullekin tuotteelle tai luokalle tilattavan nimikemäärän rajoitukset. Käytettävissä olevat arvot ovat **Käytössä B2B-asiakkaille**, **Käytössä B2C-asiakkaille**, **Käytössä kaikille asiakkaille** ja **Pois käytöstä kaikilta asiakkailta**.

> [!NOTE]
> Kun päivität moduulikirjaston uusimmaksi versioksi, sinun on varmistettava lisävaiheiden avulla, että aiemmin kuvatut sivuston asetukset ovat käytettävissä ympäristössäsi. Lisätietoja on kohdassa [Päivitä app.settings.json-tiedosto](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)file.

## <a name="create-business-partner-sign-up-pages"></a>Yrityskumppanin kirjautumissivujen luominen

Voidakseen olla yrityskumppani, käyttäjien on ensin lähetettävä yrityskumppanipyyntö. B2B-kotisivulla on linkki liikekumppanin pyyntösivulle, joten käyttäjät voivat aloittaa prosessin. Kun käyttäjät ovat lähettäneet liikekumppanipyynnön, he saavat vahvistuksen pyynnön lähettämisestä. 

### <a name="create-a-business-partner-request-page"></a>Luo liikekumppanipyyntö -sivu

**Kumppanien rekisteröityminen** -moduulia käytetään liikekumppanien pyyntösivulla, kun käyttäjäpyyntöjä lähetetään liikeyhteistyökumppaniksi. Tässä moduulissa voit kerätä kirjautumisprosessissa tarvittavat käyttäjätiedot. Lisäksi **Yritystilin osoite** -moduulin avulla siepataan käyttäjän osoite.

Noudattamalla seuraavia ohjeita voit asentaa ja määrittää liikekumppanin pyyntösivun sivustonmuodostajassa.

1. Luo malli, jonka nimi on **Rekisteröityminen**. Tämän mallin tulee sisältää seuraavat moduulit:

    - Kumppanin rekisteröityminen
    - Navigointipolku
    - Otsikko
    - Alatunniste
    - Sisältölohko
    - Tekstilohko
    - Tuotekokoelma

1. Luo **Rekisteröityminen**-mallin avulla sivu, jonka nimi on **Yrityskumppanipyyntö**.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-kohtaan **Kontti**-moduuli. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Lisää **Kontti**-paikkaan **Navigointipolku**-moduuli. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdasta aloitussivun linkki ja kirjoita linkin tekstiksi **Aloitussivu**.
1. Lisää **Kontti**-paikassa **Kumppanin rekisteröityminen** -moduuli **Navigointipolku**-moduulin alapuolelle. Kirjoita moduulin ominaisuusruudun **Otsikko**-kohdassa **Ryhdy liikekumppaniksi**.
1. Lisää **Kumppanin rekisteröityminen** -kohtaan **Yritystilin osoite**-moduuli.
1. Lisää **Kontti**-paikassa **Tekstilohko** -moduuli **Kumppanin rekisteröityminen** -moduulin alapuolelle. Tässä voit määrittää joitakin kirjautumisprosessin ehtoja.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Julkaise sivun URL-osoite.

### <a name="create-a-business-partner-request-confirmation-page"></a>Luo liikekumppanipyynnön vahvistussivu

Kun liikekumppanipyyntö on lähetetty, käyttäjälle tulee näkyviin vahvistussivu, jossa ilmoitetaan lähetyksestä. 

Noudattamalla seuraavia ohjeita voit asentaa ja määrittää pyynnön vahvistussivun sivustonmuodostajassa.

1. Luo aiemmin luodun **Rekisteröityminen**-mallin avulla sivu, jonka nimi on **Kumppanipyynnön vahvistus**.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-kohtaan **Kontti**-moduuli. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Lisää **Kontti**-paikkaan **Sisältölohko**-moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Pyyntö lähetetty**. Kirjoita **RTF-teksti**-kenttään **Pyyntösi on lähetetty**. Konfiguroi **Linkit**-kohdassa aloitussivun linkki ja kirjoita linkin tekstiksi **Jatka ostoksia**.
1. Lisää toinen **Kontti**-moduuli ja lisää siihen **Tuotekokoelma**-moduuli.
1. Konfiguroi **Tuotekokoelma**-moduuli niin, että sivulla näkyvät haluamasi suositukset tai luokkaluettelot.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Julkaise sivun URL-osoite.

Noudattamalla seuraavia ohjeita voit lisätä linkin pyynnön vahvistussivuun sivustonmuodostajassa.

1. Siirry aiemmin luomallesi **Yrityskumppanipyyntö**-sivulle ja valitse **Muokkaa**. 
1. Valitse **Kumppanin rekisteröityminen** -moduulin paikka. Määritä aiemmin luomallesi liikekumppanin pyyntösivulle linkki ominaisuusruudun **Linkki rekisteröitymisvahvistussivulle** -kohdassa. 
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Liikekumppanipyynnön linkin lisääminen kotisivulle

Kun liikekumppanipyynnön rekisteröitymis- ja vahvistussivut on luotu, rekisteröitymissivu on asetettava saataville kotisivun linkin kautta. Voit suorittaa tämän tehtävän lisäämällä linkin aloitussivulla mihin tahansa **Sisältölohko**-moduuliin.

Noudattamalla seuraavia ohjeita voit lisätä yrityskumppanipyynnön linkin aloitussivuun sivustonmuodostajassa.

1. Siirry sivuston aloitussivulle ja valitse **Muokkaa**.
1. Valitse **Sisältölohko** -moduulin paikka. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdassa linkki aiemmin luomaasi liikekumppanin pyyntösivuun ja määritä sitten **Rekisteröidy liikekumppaniksi** tai vastaava teksti linkkitekstiksi. Lisää kuva tarpeen mukaan.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

## <a name="account-management-landing-page"></a>Tilinhallinnan saapumissivu

Tilihallinnan aloitussivu sisältää kaikki tilinhallinnan tiedot, joita sekä B2B- että B2C-verkkokauppasivusto edellyttää. Vain kirjautuneet käyttäjät voivat tarkastella tätä sivua.

Toimi seuraavasti, kun haluat luoda ja konfiguroida B2B-tilinhallinnan aloitussivun sivustonmuodostajan avulla.

1. Luo malli, jonka nimi on **Tilin hallinta**. Tämän mallin tulee sisältää seuraavat moduulit:

    - Otsikko
    - Alatunniste
    - Navigointipolku
    - Tilin tervetuloruutu
    - Tilin yleinen ruutu
    - Tilin osoite -ruutu
    - Tilin toivelistaruutu
    - Tilin osoiteruutu
    - Tilin kanta-asiakkuusruutu
    - Tilin asiakassaldo -ruutu
    - Tilin tilausmallit -ruutu
    - Organisaatiokäyttäjät
    - Yrityksen organisaatioluettelo
    - Asiakastilin saldo
    - Tilausmallin rivit
    - Tilausmallin luettelo
    - Tilin lasku -ruutu
    - Laskuluettelo
    - Laskun tiedot

1. Luo **Tilin hallinta** -mallin avulla sivu, jonka nimi on **Oma tili**.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-kohtaan **Kontti**-moduuli. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**. 
1. Lisää **Kontti**-paikkaan **Navigointipolku**-moduuli. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdasta aloitussivun linkki ja kirjoita linkin tekstiksi **Aloitussivu**.
1. Lisää **Kontti**-paikkaan **Tervetuloa-ruutu**-moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Tervetuloa**.
1. Lisää **Pää**-paikkaan toinen **Kontti**-moduuli (**Kontti 2**). Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**. Määritä **Näytetyt alitasot** -arvoksi **Kaksi**. 
1. Lisää **Kontti 2** -paikkaan **Tilin yleinen ruutu** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Oma profiili**. Määritä **Linkit**-kohdassa linkki **Oma profiili** -sivulle. 
1. Lisää **Kontti 2** -paikkaan toinen **Tilin yleinen ruutu** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Tilaushistoria**. Määritä **Linkit**-kohdassa linkki tilaushistoriasivulle.
1. Lisää **Pää**-paikkaan kolmas **Kontti**-moduuli (**Kontti 3**). Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**. Määritä **Näytetyt alitasot** -arvoksi **Kaksi**. 
1. Lisää **Kontti 3** -paikkaan **Tilin osoite -ruutu** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Oma osoite**. Määritä **Linkit**-kohdassa linkki **Oma osoite** -sivulle. 
1. Lisää **Kontti 3** -paikkaan **Toivomuslistaruutu** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Oma toivomuslista**. Määritä **Linkit**-kohdassa linkki **Oma toivomuslista** -sivulle.
1. Lisää **Pää**-paikkaan neljäs **Kontti**-moduuli (**Kontti 4**). Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**. Määritä **Näytetyt alitasot** -arvoksi **Kaksi**. 
1. Lisää **Kontti 4** -paikkaan **Organisaation käyttäjät** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Organisaation käyttäjät**. 
1. Lisää **Kontti 4** -paikkaan **Asiakkaan saldo -ruutu** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Tilin luotto**. 
1. Lisää **Pää**-paikkaan viides **Kontti**-moduuli (**Kontti 5**). Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**. Määritä **Näytetyt alitasot** -arvoksi **Kaksi**. 
1. Lisää **Kontti 5** -moduuliin **Tilin tilausmallit -ruutu** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Tilausmallit**. 
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

> [!NOTE] 
> Jotkin vaiheissa 13–18 lisätyt osat eivät näy sivustonmuodostimen WYSIWIG-pohjassa, koska ne edellyttävät sisäänkirjautunutta B2B-tiliä.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Asiakkaan saldosivujen ja -moduulien luominen ja konfiguroiminen 

Asiakastilejä voidaan käyttää tilausten maksuun. Asiakastilin käytettävissä olevaa saldoa voidaan tarkastella käyttäjän tilinhallintasivulta.

### <a name="create-a-customer-balance-page"></a>Asiakkaan saldosivun luonti 

Ennen kuin kirjautuneet B2B-käyttäjät voivat tarkastella asiakkaan saldoa, sinun on luotava asiakkaan saldosivu. 

Luo asiakkaan saldosivu sivustonmuodostimessa seuraavasti.

1. Luo **Asiakkaan saldo** -niminen sivu käyttämällä aiemmin luomaasi **Tilin hallinta** -mallia.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-paikkaan kolmas **Kontti**-moduuli (**Kontti 3**). Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**. Määritä **Näytetyt alitasot** -arvoksi **Kaksi**.
1. Lisää **Kontti**-paikkaan **Navigointipolku**-moduuli. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdasta tilihallinnan aloitussivun linkki ja kirjoita linkin tekstiksi **Oma tili**.
1. Lisää **Kontti** -paikkaan **Asiakastilin saldo** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Tilin saldo**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Julkaise sivun URL-osoite.
1. Siirry aiemmin luomallesi tilinhallinnan aloitussivulle (**Oma tili**).
1. Lisää linkki asiakkaan saldosivulle **Asiakkaan saldo -ruutu** -moduulin ominaisuusruudussa. 
1. Tallenna ja julkaise sivu.

Asiakkaan saldosivu on nyt luotu, ja käyttäjät voivat käyttää sitä tilinhallinnan aloitussivulta.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Määritä uloskuittaamisen sivu siten, että asiakkaan saldoa voi käyttää maksutapana.

**Asiakastilin maksu** -moduuli on pakollinen, jotta asiakkaan saldoa voi käyttää maksutapana. Tämä moduuli tulee lisätä uloskuittaussivulle maksutavaksi. Lisätietoja uloskuittaussivun määrittämisestä ja uloskuittauksen edellyttämistä moduuleista sekä kaikista maksun tiedoista on kohdassa [Uloskuittausmoduuli](../add-checkout-module.md).

Kun olet konfiguroinut uloskuittaussivun, lisää **Asiakastilin maksu** -moduuli maksuosaan ja tallenna ja julkaise sivu. B2B-käyttäjät voivat tällöin kirjautua sisään sähköisen kaupankäynnin sivuston ja käyttää käytettävissä olevaa asiakassaldoa tilauksiin uloskuittauksen aikana.

Lisäksi kohdassa **Sivustonmuodostin \> Laajennukset** on varmistettava, että **Ota käyttöön asiakastilin maksut** -ominaisuuden arvoksi on määritetty **Käytössä B2B-asiakkaille**.

## <a name="create-order-template-pages"></a>Tilausmallisivujen luominen

B2B-verkkokauppasivustoa varten voi määrittää kaksi tilausmallisivua: tilausmallien luettelosivun ja tilausmallirivien sivun.

Tilausmallien luettelosivulla näkyy luettelo kaikista käytettävissä olevista tilausmalleista. Se määritetään **Tilausmalliluettelo**-moduulin avulla. Tilausmallien luettelosivun avulla voit luoda tai poistaa mallin ja lisätä mallin nimikkeitä ostoskoriin.

Tilausmallirivien sivulla näkyvät tilausmallien luettelosivulla valitun tilausmallin tiedot. Se määritetään **Tilausmallirivit**-moduulin avulla. Kun käyttäjä valitsee mallin nimen tilausmallien luettelosivulta, näkyviin tulee tilausmallirivien sivu, jossa näkyvät mallin tiedot. Käyttäjä voi tämän jälkeen tarkastella ja muokata mallin nimikkeitä.

### <a name="create-an-order-templates-list-page"></a>Tilausmallien luettelosivun luominen

Luo tilausmallien luettelosivu sivustonmuodostimessa seuraavasti.

1. Luo **Tilausmallit** -niminen sivu käyttämällä aiemmin luomaasi **Tilin hallinta** -mallia.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-kohtaan **Kontti**-moduuli. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Lisää **Kontti**-paikkaan **Navigointipolku**-moduuli. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdasta tilihallinnan aloitussivun linkki ja kirjoita linkin tekstiksi **Oma tili**.
1. Lisää **Kontti** -paikkaan **Tilausmalliluettelo**-moduuli.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Julkaise sivun URL-osoite.
1. Siirry aiemmin luomallesi tilinhallinnan aloitussivulle (**Oma tili**).
1. Määritä juuri luomaasi tilausmallien luettelosivuun linkki **Linkit**-kohdan **Tilin tilausmallit -ruutu**-moduulin ominaisuusruudussa.
1. Tallenna ja julkaise sivu.

Tilausmallien luettelosivu on nyt luotu, ja käyttäjät voivat käyttää sitä tilinhallinnan aloitussivulta.

### <a name="create-an-order-template-lines-page"></a>Tilausmallirivien sivun luominen

Luo tilausmallirivien sivu sivustonmuodostimessa seuraavasti.

1. Luo **Tilausmallirivit** -niminen sivu käyttämällä aiemmin luomaasi **Tilin hallinta** -mallia.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-kohtaan **Kontti**-moduuli. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Lisää **Kontti**-paikkaan **Navigointipolku**-moduuli. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdasta tilihallinnan aloitussivun linkki ja kirjoita linkin tekstiksi **Oma tili**.
1. Lisää **Kontti**-paikkaan **Tilausmallirivit**-moduuli.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Julkaise sivun URL-osoite.

## <a name="onboard-business-partner-users"></a>Liikekumppanikäyttäjien perehdyttäminen

Organisaation käyttäjäsivun avulla yrityskumppaniorganisaation järjestelmänvalvoja voi ottaa lisäkäyttäjiä tästä organisaatiosta B2B-verkkokauppasivustoon. Se määritetään **Yrityksen organisaatioluettelo**-moduulin avulla. Järjestelmänvalvoja voi lisätä tai poistaa käyttäjiä organisaation käyttäjäsivulta, määrittää tilien saldoja ja pyytää käyttäjän tiliotteita.

Luo organisaation käyttäjien sivu sivustonmuodostimessa seuraavasti.

1. Luo **Organisaation käyttäjät** -niminen sivu käyttämällä aiemmin luomaasi **Tilin hallinta** -mallia.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-kohtaan **Kontti**-moduuli. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Lisää **Kontti**-paikkaan **Navigointipolku**-moduuli. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdasta tilihallinnan aloitussivun linkki ja kirjoita linkin tekstiksi **Oma tili**.
1. Lisää **Kontti** -paikkaan **Yrityksen organisaatioluettelo** -moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Organisaation käyttäjät**.
1. Ota **Yrityksen organisaatioluettelo** -moduulin ominaisuusruudussa käyttöön **Taulujen lajittelu**- ja **Taulujen sivutus** -ominaisuudet. Määritä sivutusmääräksi **5**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Julkaise sivun URL-osoite.
1. Siirry aiemmin luomallesi tilinhallinnan aloitussivulle (**Oma tili**).
1. Määritä juuri luomaasi organisaation käyttäjäsivuun linkki **Linkit**-kohdan **Organisaation käyttäjät -ruutu**-moduulin ominaisuusruudussa. 
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

## <a name="create-invoice-pages"></a>Laskusivujen luominen

Laskujen luettelosivulla näkyy kaikkien käytettävissä olevien laskujen luettelo. Se määritetään **Laskuluettelo**-moduulin avulla. Laskuluettelosivulta käyttäjät voivat maksaa tai pyytää laskuja. 

Laskun tietosivulla näkyvät laskujen luettelosivulla valitun laskun tiedot. Se määritetään **Laskun tiedot**-moduulin avulla. Kun käyttäjä valitsee laskun tunnuksen laskuluettelosivulta, laskun tietosivu tulee näkyviin ja näyttää laskun tiedot.

### <a name="create-an-invoices-list-page"></a>Laskuluettelosivun luominen

Luo laskuluettelosivu sivustonmuodostimessa seuraavasti.

1. Luo **Laskuluettelo** -niminen sivu käyttämällä aiemmin luomaasi **Tilin hallinta** -mallia.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-kohtaan **Kontti**-moduuli. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Lisää **Kontti**-paikkaan **Navigointipolku**-moduuli. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdasta tilihallinnan aloitussivun linkki ja kirjoita linkin tekstiksi **Oma tili**.
1. Lisää **Kontti**-paikkaan **Laskuluettelo**-moduuli. Kirjoita moduulin ominaisuusruudun **Otsikko**-ruutuun **Laskut**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Julkaise sivun URL-osoite.
1. Siirry aiemmin luomallesi tilinhallinnan aloitussivulle (**Oma tili**).
1. Määritä juuri luomaasi laskuluettelosivuun linkki **Linkit**-kohdan **Tilin laskut -ruutu**-moduulin ominaisuusruudussa. 
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

### <a name="create-an-invoice-details-page"></a>Laskun tietosivun luominen

Luo laskun tietosivu sivustonmuodostimessa seuraavasti.

1. Luo **Laskun tiedot** -niminen sivu käyttämällä aiemmin luomaasi **Tilin hallinta** -mallia.
1. Lisää **Otsikko**-kohtaan katkelma, joka on valmiiksi määritetty sivuston otsikon avulla.
1. Lisää **Alatunniste**-kohtaan katkelma, joka on valmiiksi määritetty sivuston alatunnisteen avulla.
1. Lisää **Pää**-kohtaan **Kontti**-moduuli. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Lisää **Kontti**-paikkaan **Navigointipolku**-moduuli. Konfiguroi moduulin ominaisuusruudun **Linkit**-kohdasta tilihallinnan aloitussivun linkki ja kirjoita linkin tekstiksi **Oma tili**. Konfiguroi sitten linkki laskujen luettelosivulle ja kirjoita **Laskuluettelot** linkin tekstiksi.
1. Lisää **Kontti**-paikkaan **Laskun tiedot**-moduuli.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Julkaise sivun URL-osoite.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](../starter-kit-overview.md)

[Muokkaussivun yleiskatsaus](../authoring-home-overview.md)

[Mallit ja asettelut – yleiskatsaus](../templates-layouts-overview.md)

[Katkelmien käyttäminen](../work-with-fragments.md)

[Uuden sivuston sivun lisääminen](../add-new-page.md)

[Kassamoduuli](../add-checkout-module.md)

[Sisältölohkomoduuli](../add-hero-module.md)

[Tuotekokoelma](../product-collection-module-overview.md)

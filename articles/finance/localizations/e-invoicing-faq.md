---
title: Sähköinen laskutus – usein kysytyt kysymykset
description: Tässä artikkelissa on tietoja sähköistä laskutusta koskevista usein kysytyistä kysymyksistä.
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: cf712c188e27deef4edfce7f5473fec4bb759bdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285814"
---
# <a name="electronic-invoicing-faq"></a>Sähköisen laskutuksen usein kysytyt kysymykset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on vastauksia sähköistä laskutuspalvelua koskeviin usein kysyttyihin kysymyksiin. Sähköinen laskutus laajentaa Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin ja Dynamics 365 Project Operationsin sähköisen laskutuksen ominaisuuksia. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Mikä on tärkeää sähköisessä laskutuksessa ja miksi se on tärkeää organisaatiolleni?

Toiminnan monimutkaisuus ja riskit kasvavat edelleen, kun organisaatiot laajentavat toimintaansa alueiden välillä. Yhteensopivuuden ylläpitäminen ja mukautuminen usein muuttuviin määräyksiin on kasavava haaste, ja se on erityisen tärkeää laskutettaessa. Laskutus on ollut perinteisesti kallista ja virhealtista, kun yritykset ovat riippuvaisia paperiasiakirjoista ja manuaalisista prosesseista.  

Organisaatiot ovat alkaneet siirtyä pois paperilaskuista kustannusten ja päästä päähän -prosessin nopeuttamiseksi. Julkishallinnon organisaatiot ovat siirtymässät sähköisen laskutuksen käyttöön verotuksen digitalisoinnin osana. Kun organisaatioiden edellytetään lähettävän digitaalisesti reaaliaikaisia verotietoja veroviranomaisille, viranomaiset voivat vähentää verojen välttelyä ja manipulointia sekä vähentää petoksia. 

Koko maailma on siirtymässä paperittomaan asiakirjakäsittelyyn ja ilman sähköistä laskutusta asiakkaat voivat ottaa riskiä yhteensopivuusongelmista, tarpeettomista kustannuksista ja kilpailijoiden jälkeen jäämisestä. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Eikö Financessa, Supply Chain Managementissa ja Project Operationsissa ole jo sähköinen laskutustoiminto? Mikä arvo tällä on minulle asiakkaana? 

Sähköinen laskutus laajentaa Financen, Supply Chain Managementin ja Project Operationsin sähköisiä laskutustoimintoja. Toiminnot myös yksinkertaistavat uusimpien sähköisten laskutusstandardien noudattamista, ja se tarjoaa yhtenäiset kokemukset eri alueilla sähköisen laskujen käsittelyn ja vaihdon suhteen. Sähköisen laskutuksen toiminnot tuovat monenlaisia etuja, joita ovat esimerkiksi seuraavat: 

   - Nopeampi ja helpompi maa-/aluekohtaisten määritysten käyttöönotto.
   - Sähköisen laskutusratkaisun käyttöönottojen standardointi. 
   - Parannettu sähköisen laskutuksen jäljitettävyys.  
   - Helpottaa lakisääteisten vaatimusten ja paikallisten liiketoimintakäytäntöjen noudattamisen ylläpitoa. 
   - Yksinkertainen ratkaisun pakkaus.
   - Skaalausominaisuudet suurille lähetettyjen tiedostojen määrälle, mikä nopeuttaa asiakirjojen kiertoa.
   - Mahdollisuus jakaa ratkaisut muiden yritysten kanssa.

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Tukeeko sähköinen laskutuspalvelu Financen, Supply Chain Managementin ja Project Operationsin paikallisia asennuksia? 

Nykyinen alusta ei salli paikallisen version käyttöä, eikä sitä ole suunnitelmia tukea tulevaisuudessa.

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>Käyttääkö sähköinen laskutuspalveluliittymä toimittajan tuonnin automaatio-ominaisuutta?

Et voi. Tätä käyttöliittymää varten on suunnitelmia, mutta suunniteltua aikajanaa ei ole. Kun niitä suunnitellaan, päivämäärät ilmoitetaan [julkaisusuunnitelmissa](/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Miten sähköinen laskutuspalvelu käsittelee sähköiseen laskuun liittyvät tiedostoliitteet? Tarvitaanko SharePoint-palvelin, kun PDF-tiedostoja upotetaan XML-tiedostoon?

Sähköiseen laskuun liitettyjä tiedostoja käsitellään XML-elementtiin upotettuina binaaritietoina. SharePoint-palvelinta ei tarvita PDF-tiedostojen upottamiseen, mutta liite on tallennettava Financen, Supply Chain Managementin tai Project Operationsin tiedostohallintajärjestelmään.

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>Onko sähköinen laskutuspalvelu käytettävissä maani/alueeni säännösten mukaan?

Sähköinen laskutuspalvelu on mikropalvelualusta, joka on käytettävissä maailmanlaajuisesti.

Microsoft aikoo julkaista sähköiset laskumuodot ja integroinnit niille maille ja alueille, joiden toiminnallisuuden Microsoft on lokalisoinut. Lisätietoja on kohdassa [Sähköisten laskutusominaisuuksien saatavuus](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Jos maasi/alueesi sähköistä laskutusmuotoa ei ole lueteltu, alusta pyrkii tukemaan tätä skenaariota tulevaisuudessa. Voit edelleen hyödyntää sähköisen laskutuksen konfiguraatiotoimintoja ja konfiguroida sähköisen laskutusmuodon itse tai voit konfiguroida organisaatiosi ominaisuudet yhdessä yhteistyökumppanin/ISV:n kanssa.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Onko Dynamics 365 for Regulatory Services uusi moduuli, kuten Human Resources tai Project Operations, joka on linkitetty Financeen tai Supply Chain Managementiin? Liittyykö tähän lisäkustannuksia?

Dynamics 365 for Regulatory Services (RCS) on pilvipalvelu globalisointiresurssien konfigurointiin. RCS on maksuton kaikille Financen, Supply Chain Managementin ja Project Operationsin lisenssin haltijoille.

Rekisteröidy RCS:sään osoitteessa <https://marketing.configure.global.dynamics.com/>.

Lisätietoja: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>Tarvitseeko rekisteröityä, jotta saan sähköisen laskutuspalvelun, vai otanko sen vain käyttöön toiminnonhallinnassa?

Jos sinulla on Financen, Supply Chain Managementin tai Project Operationsin käyttöoikeus, rekisteröidy sähköiseen laskutukseen kohdassa [Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md).

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Toimiiko sähköinen laskutuspalvelu tason 1 näennäiskoneiden kanssa? Mikä on edellytetty vähimmäisympäristö?

Sähköisen laskutuspalvelun integrointi edellyttää vähintään tason 2 näennäiskonetta Financen tai Supply Chain Managementin isännöintiin. Lisätietoja ympäristöjen suunnittelusta on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>Onko sähköisessä laskutuspalvelussa testitila laskun lähetyksen testaamista varten?

Tämä voidaan saavuttaa konfiguraation avulla. Voit testata laskun lähettämistä muodostamalla yhteyden Financeen tai Supply Chain Managementiin käyttäjän hyväksynnän testiympäristöstä (UAT) ja lähettää testilaskut. Sähköinen laskutus tukee digitaalisten testisertifikaattien konfigurointia ja digitaalista hyväksyntää edellyttävissä sähköisissä laskuissa veroviranomaisten julkaisemien testiverkkopalveluiden URL-osoitteiden määritystä.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Onko olemassa dokumentaatiota sähköisistä laskutuksen käyttövalmiista maa-/aluekohtaisista ominaisuuksista?

Kyllä. Tietoja sähköisten laskutusominaisuuksien saatavuudesta ja niiden tukemista muodoista on kohdassa [Sähköisten laskutusominaisuuksien käytettävyys](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>Salliiko sähköinen laskutuspalvelu Financessa tai Supply Chain Managementissa olevan yrityksen, joka on määritetty tietylle maalle, käyttää sähköisen laskutuksen ominaisuuksia muista maista / muilta alueilta?

Kyllä. Sähköisiä laskutusominaisuuksia voidaan käyttää yritysasiakirjojen lähettämisen käsittelyyn yrityksen maasta riippumatta seuraavissa tapauksissa:

   - Luotavassa liiketoiminta-asiakirjassa käytetään sopivaa tiedostomallin määritystä.
   - Liiketoimintatiedostossa ja sähköisessä laskutusominaisuudessa määritetyt käytettävyyssäännöt täsmäävät.

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>Käyttääkö sähköinen laskutuspalvelu samaa konfiguraatiota ja suunnittelukokemusta, jotka ovat Financen ja Supply Chain Managementin sähköisen raportointimoduulin käytössä? 

Kyllä. Samoja suunnittelutyökaluja, joita käytetään Financen ja Supply Chain Managementin Sähköisen raportoinnin (ER) moduulissa, käytetään myös tietomallien määrityksen ja tiedostomuodon konfiguraatioiden luomisessa ja konfiguroinnissa. Näitä suunnittelutyökaluja käytetään myös Regulatory Configuration Services (RCS) -palveluissa tietomallien määrityksen ja tiedostomuodon konfiguraatioiden luomisessa ja konfiguroimisessa.

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>Voiko käytettävyyssääntöjä laajentaa ja konfiguroida niin, ettei niitä ole sidottu mihinkään tiettyyn parametriin, kuten yritykseen?

Kyllä. Käytettävyyssäännöt ovat täysin konfiguroitavissa. Voit lisätä tai poistaa lausekkeita, muodostaa logiikan toimintoja sekä ryhmitellä lausekkeita ja poistaa ryhmityksiä. Lisätietoja on kohdassa [Soveltuvuussäännöt](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules).

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>Tukeeko sähköinen laskutuspalvelu muiden ER-muotoisten konfiguraatioiden lisäämistä muiden tiedostotyyppien luomiseksi? Tukeeko se tiedostojen lähettämistä sähköisesti asiakkaille, esimerkiksi toimitusilmoituksia?

Voit käyttää muita ER-muotoisia konfiguraatioita haluttujen tulostustiedostojen tuottamiseen. ER-muotoinen konfigurointi on kuitenkin johdettava samasta ER-laskumallin määrityksestä, joka on määritetty Financessa tai Supply Chain Managementissa liiketoimintatiedostojen muodostamista varten. Sähköinen laskutus ei tue valmiina tulostiedoston lähettämistä suoraan asiakkaalle EDI-tapahtumana.

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>Tukeeko sähköinen laskutuspalvelu sähköisten laskujen vaihtamista asiakkaiden kanssa? Tukeeko se eri laskumuotojen konfiguroimista samalle laskulle?

Toimittajien sähköisten laskujen vastaanotto- ja tuontitoiminto on toteutussuunnitelmassa, mutta sähköisten laskujen lähettämistä asiakkaille automaattisesti ei tueta tällä hetkellä.

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>Tukeeko sähköinen laskutuspalvelu EDI-sanomien vaihtamista toisten yritysten kanssa?

Sähköisen laskutuspalvelun painopiste on sähköisten laskusanomatyyppien vaihto, joka perustuu määräysten vaatimustenmukaisuusvaatimuksiin. Sähköisten laskujen vastaanottaminen ja niiden tuominen toimittajilta on toteutussuunnitelmassa, mutta sähköisten laskutiedostojen lähettämistä asiakkaille ei tueta tällä hetkellä valmiiksi, elleivät säädökset edellytä sähköisen laskun lähettämistä asiakkaalle.

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>Tukeeko sähköinen laskutuspalvelu ER-muotoisiin konfigurointiin perustuvien mukautusten tuomista tai yhdistämistä vanhasta sähköisestä laskutuksesta?

Sähköisessä laskutuspalvelussa voit käyttää ER-muotoisia konfiguraatioita uudelleen. ER-muotoinen konfigurointi on kuitenkin johdettava samasta ER-laskumallin määrityksestä, jota sähköinen laskutustoiminto oli suunniteltu käyttämään ja joka on määritetty Financessa tai Supply Chain Managementissa liiketoimintatiedostojen muodostamista varten.

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>Tukeeko sähköinen laskutuspalvelu sähköisten laskujen myöntämistä räätälöidyistä taulukoista? Jos kyllä, miten näille uusille taulukoille ja yksiköille luodaan ER-tietomallikonfiguraatiot?

Kyllä. Se edellyttää kuitenkin laskumallin määrityksen mukauttamista ja tarvittavien viitteiden lisäämistä mukautettuihin taulukoihin, tai monimutkaisuudesta riippuen uuden laskumallin yhdistämismäärityksen luomista.

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>Tukeeko sähköinen laskutuspalvelu erilaisia verkkopalvelun päätepisteitä?

Sähköinen laskutuspalvelu tukee erilaisia verkkopalvelun päätepisteitä. Voit käyttää konfiguroitavaa integrointia REST-verkkopalveluiden kanssa tai useita maakohtaisia verkkopalveluintegrointeja. Samalle verkkopalvelulle ja ohjelmointirajapinnoille voidaan konfiguroida erilaisia päätepisteitä käyttämällä eri konfiguraatioversioita. Katso lisätietoja osasta [Toimikohtainen parametriluettelo](e-invoicing-setup.md#list-of-parameters-by-action).

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>Integroidaanko sähköinen laskutus eri laskujen operaattoreiden ohjelmointirajapintoihin Pohjoismaista vai tulisiko niitä käsitellä tapauskohtaisesti?

Microsoft laajentaa toimintojen kattavuutta jatkuvasti valmiiden integrointien tarjoamiseksi sähköisten laskutusominaisuuksien avulla. Lisätietoja tuetuista muodoista ja integroinneista on kohdassa [Sähköisten laskutusominaisuuksien käytettävyys](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Jos et löydä etsimääsi vastausta, lähetä kysymyksesi tuotekehitystiimille osoitteeseen <D365EInvoicePreview@microsoft.com>. Microsoft joko ottaa yhteyttä tai parantaa näiden usein kysyttyjen kysymysten kattavuutta.

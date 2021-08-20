---
title: Tuotetietojen vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotetietojen käytössä voi esiintyä.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5b74c1a769b3f0c3b848a034ed3d1bab76fda7eb5d8d62f4b3608d8706c696dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778647"
---
# <a name="troubleshoot-product-information"></a>Tuotetietojen vianmääritys

Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotetietojen käytössä voi esiintyä.

## <a name="i-cant-delete-a-released-product"></a>Vapautettua tuotetta ei voi poistaa

### <a name="issue-description"></a>Ongelman kuvaus

Vapautetun tuotteen ja kaikki sen variantit voidaan poistaa vain, jos vapautetussa tuotteessa ei ole liittyviä tapahtumia.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Poista vapautettu tuote tai päätuote seuraavasti:

1. Sulje kaikki nimikkeiden avoimet tapahtumat.
1. Vähennä varaston arvoksi 0 (nolla).
1. Suorita varaston sulkeminen.
1. Poista kaikki poistettavan päätuotteen tuotevariantit.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Voiko vapautetun tuotteen nimiketunnuksen vaihtaa?

Useimmissa tapauksissa vapautettujen tuotteiden nimiketunnuksia ei voi muokata, koska tiedot vaurioituisivat muutoksen vuoksi. Nimiketunnusta voi muokata vain, jos on korjattava vapautetun tuotteen ensisijaisen avaimen uudelleennimeämisen aiheuttama tietojen vaurioituminen. Tästä oli maininta [Finance and Operations 10.0.0:n ja Platform update 24:n poistettujen tai vanhentuneiden toimintojen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24) luettelossa.

Jos haluat mahdollisuuden muokata vapautettujen tuotteiden nimiketunnusta, [äänestä ideaa ideaportaalissa](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Tuotteen oletusmateriaaliottosääntöä ei anneta tuoterakenneriville.

### <a name="issue-description"></a>Ongelman kuvaus

Kun nimike lisätään tuoterakenneriville, järjestelmä ei käytä nimikkeelle määritettyjä oletusmateriaaliottosäännön tietoja. Nimikkeen materiaaliottosääntö ei siis näytä **Tuoterakenteen rivi** -sivulla.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Jos määrität materiaaliottosäännön tuoterakennerivillä, sitä käytetään kyseisellä tuoterakennerivillä. Jos materiaaliottosääntö on kuitenkin tyhjä tai jos sitä ei määritä tuoterakennerivillä, nimikkeellä määritettyä materiaaliottosääntöä käytetään siltä kyseisellä tuoterakennerivillä, vaikka sitä ei kyseisellä rivillä näytetä.

Muiden Microsoft Dynamics 365 Supply Chain Managementin toimintojen oletuslogiikka ei yleensä toimi tällä tavalla. Nykyistä toimintaa ei kuitenkaan voi muuttaa. Muutoin tietyt siihen perustuvat aiemmin luodut mukautukset saattaisivat lakata toimimasta.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Järjestelmä sallii viivakoodien kaksoiskappaleiden tallentamisen eri nimikkeille tai samalle nimikkeelle, jolla on eri dimensiot

Järjestelmä ei tällä hetkellä pakota käyttämään yksilöiviä viivakoodeja ja tämän rajoituksen lisääminen olisi häiriöitä aiheuttava muutos. Microsoftilla on itse asiassa tieto siitä, että tämä muutos aiheuttaisi joidenkin aiemmin luotujen asiakasasennusten rikkoutumisen. Laajaa uudelleensuunnittelua kuitenkin pohditaan, jotta tämä toiminto olisi mahdollinen tulevaisuudessa.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Nimiketietuemallia muokatessa avautuu seuraava virhesanoma: Varastosijaintia ei voi luoda, koska nimikettä ei ole varastoitu. Jotta voit varastoida nimikkeitä, liitetyn nimikemalliryhmän Varastoitu tuote -asetuksen on oltava valittuna.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma esiintyy, jos yrität luoda näiden ohjeiden mukaan mallin nimikkeelle, jota ei ole varastoitu.

1. Avaa vapautettu tuote, jota ei ole varastoitu.
1. Valitse toimintoruudun **Asetukset**-välilehdessä **Tietueen tiedot**.
1. Valitse **Tietueen tiedot** -valintaikkunassa **Yrityksen tilien malli**.

Tässä tapauksessa avautuu seuraava virhesanoma:

> Varastosijaintia ei voi luoda, koska nimikettä ei ole varastoitu Jotta voit varastoida nimikkeitä, liitetyn nimikemalliryhmän Varastoitu tuote -asetuksen on oltava valittuna.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tuotemallien luontiprosessi edellyttää tuotekohtaista lisälogiikkaa. Tämän vuoksi tässä yhteydessä ei voi käyttää yleistä **Yrityksen tilien malli** -painiketta. Toimi sen sijaan seuraavasti:

1. Avaa vapautettu tuote.
1. Valitse toimintoruudun **Tuote**-välilehden **Uusi**-ryhmässä **Malli \> Luo jaettu malli**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Tuotemääritteisiin lisättävää oletusohjetekstiä ei ole vapautetussa tuotteessa.

Tuotemääritteisiin lisättävä kuvaus ja ohjeteksti eivät näy tai niitä ei oletusarvoisesti anneta vapautetuissa tuotteissa. Tämä on suunniteltu ominaisuus.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Annettu oletusmäärä vaihtelee sen mukaan, rekisteröidäänkö se tuoterakenteesta vai tuoterakenteen versiosta

### <a name="issue-description"></a>Ongelman kuvaus

Kun nimike lisätään tuoterakenteeseen, määräksi määritetään oletusarvoisesti 1 eikä valitun tuotteen **Tilauksen oletusasetukset** -sivun **Väh.tilausmäärä** -kentässä määritetty määrä. Jos nimike kuitenkin lisätään tuoterakenneversiosta ja nimike ja variantti valitaan, oletusarvoisesti annettava määrä ottaa huomioon tiettyjen dimensioiden tilauksen oletusasetuksissa määritetyn vähimmäismäärän.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä toiminta on tarkoituksellista. Tuoterakenteen ja tuoterakenteen version välinen logiikkaero on kuitenkin tunnettu ongelma. Tätä toimintaa ei siitä huolimatta tulla muuttamaan, koska muutos voisi vaikuttaa moniin erilaisiin asiakasskenaarioihin.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>Tuotteen asiakirjaliitteiden tietoentiteetistä ladattuja liitettyjä kuvia ei vaihtaa vapautetun tuotteen tiedoissa

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma voi esiintyä, kun kuva liitetään nimikkeeseen *Tuotteen asiakirjaliitteet* -tietoentiteetin avulla. Tässä tapauksessa nimikkeen kuva näytetään nimikkeelle. Jos kuitenkin valitaan **Vaihda kuva**, ladattujen kuvien luettelossa ei ole mitään. Myöskään liitteitä ei näytetä nimikkeelle.

### <a name="issue-resolution"></a>Ongelman ratkaisu

*EcoResProductDocumentAttachmentEntity*-entiteetti (*Tuotteen asiakirjaliitteet*) tuo *tuotteiden* mutta ei *vapautettujen tuotteiden* asiakirjaliitteet. (Vapautettuja tuotteita kutsutaan myös *nimikkeiksi*.) Nimikkeen liitteiden tarkasteleminen **Vapautetun tuotteen tiedot** -sivulla onnistuu, kun käytössä on *EcoResReleasedProductDocumentAttachmentEntity*-entiteetti (*Vapautetun tuotteen asiakirjaliitteet*).

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Microsoft Flow -yhdistimessä avautuu seuraava virhesanoma: Päivitystä ei sallita kentälle ProductNumber.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma esiintyy, jos **Tuotenumero**-kenttä päivitystä yritetään *Vapautetut tuotteet* -entiteetin V2 ja Microsoft Flow'n avulla.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä toiminta on tarkoituksellista. Mahdollisuus muokata vapautetun tuotteen tuotenumeroa poistettiin Dynamics 365 Finance and Operations 10.0.0:n platform update 24:stä, koska näin haluttiin estää tietojen vioittuminen. Poikkeustapauksissa, joissa on korjattava vapautetun tuotteen ensisijaisen avaimen aiemman uudelleennimeämisen aiheuttama tietojen vioittuminen, Microsoft-tukea voidaan pyytää poistamaan tämä rajoitus tilapäisesti.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Vapautetun tuotevariantin luominen ei onnistu toisessa yrityksessä

### <a name="issue-description"></a>Ongelman kuvaus

Jos päätuote yritetään vapauttaa ilman variantteja ja sitten variantteja yritetään luoda tarpeen mukaan kussakin yrityksessä, variantteja voi vapauttaa varianttiehdotuksia käyttämällä. Variantteja ei myöskään voi luoda manuaalisesti.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus. Päätuotteen ja päätuotteen käyttämien dimensioiden suhteita säilytetään jaetulla tasolla. Niinpä jaetun päätuotteen käytettävissä olevia dimensioita ei voi luoda tietyssä yrityksessä, jossa kyseiset dimensiot vapautetaan, ja sitten replikoida prosessia kussakin yrityksessä, jossa dimensioita tarvitaan. Sen sijaan vapautusprosessi on muutettava mukautumaan suunniteltuun prosessiin.

Tuotteiden vapauttamisprosessi:

1. Luo jaettu päätuote ja dimensiot, jotka voidaan vapauttaa yrityksiin.
1. Vapauta tuotteet yrityksiin, joka käyttämällä varianttiehdotuksia ja manuaalisesti lisäämällä vapautettavat yhdistelmät.

Vaihtoehtoiesti voit luoda vapautetun tuotteen myös suoraan.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Kun variantti vapautetaan toisessa yrityksessä seuraava virhesanoma avautuu: Tuotevariantti, jolla on määritetyt dimensiot, on jo luotu.

### <a name="issue-description"></a>Ongelman kuvaus

Jos tuotevariantti on jo vapautettu yrityksessä A ja yrität vapauttaa sen yrityksessä B käyttämällä **Uusi**-painiketta **Vapautetut tuotevariantit** -sivulla, seuraava virhesanoma avautuu:

> Tuotevariantti, jolla on määritetyt dimensiot, on jo luotu.

### <a name="issue-resolution"></a>Ongelman ratkaisu

**Vapautetut tuotevariantit** -sivun **Uusi**-painike luo variantin ja vapauttaa sen yrityskontekstissa. Jos variantti on jo luotu, sitä ei voi vapauttaa toisessa yrityksessä **Uusi**-painikkeella.

Korjaa ongelma vapauttamalla aiemmin luotu variantti toivotussa yrityksessä avaamalla **Päätuote**-sivu ja valitsemalla **Vapauta tuote**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
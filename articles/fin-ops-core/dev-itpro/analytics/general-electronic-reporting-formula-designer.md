---
title: Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto
description: Tässä artikkelissa on tietoja siitä, miten käyttää kaavasuunnittelijaa sähköisessä raportoinnissa (ER).
author: NickSelin
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b03613cb40c5ca718f45e69740d29059fcfb70b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894292"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten kaavojen suunnittelutoimintoa käytetään sähköisessä raportoinnissa (ER). Kun tietyn sähköisen asiakirjan muotoa suunnitellaan ER:ssä, voit muuntaa tiedot kaavojen avulla vastaamaan asiakirjan toteuttamis- ja muotoiluvaatimuksia. Nämä kaavat muistuttavat Microsoft Excelin kaavoja. Kaavoissa tuetaan erilaisia toimintoja: teksti, päivämäärä ja aika, matemaattiset ja loogiset funktiot, tiedot ja tietotyyppien muunnostoiminnot ja myös muut liiketoiminnan toimialuekohtaiset toiminnot.

## <a name="formula-designer-overview"></a>Yleiskatsaus kaavan suunnittelutoimintoon

Sähköinen raportointi tukee kaavojen suunnittelutoimintoa. Tämän vuoksi voit määrittää suunnittelun yhteydessä lausekkeita, joita voidaan käyttää suorituksen aikana seuraavissa tehtävissä:

- Sovelluksen tietokannasta vastaanotettujen tietojen muuntaminen. Tiedot täytetään ER-tietomalliin, joka on suunniteltu ER-muotojen (kuten suodatus, ryhmittely ja tietotyypin muunnos) tietolähteeksi. (Näitä muunnoksia ovat esimerkiksi suodatus, ryhmitys ja tietotyypin muunto.)
- Muodostettavaan sähköiseen asiakirjaan lähetettävien tietojen muotoilu tietyn ER-muodon asettelun ja ehtojen mukaisesti. (Muotoilu voidaan tehdä esimerkiksi pyydetyn kielen tai kulttuurin tai koodauksen mukaisesti.)
- Sähköisten asiakirjojen luontiprosessin hallinta. (Lausekkeet voivat esimerkiksi ottaa käyttöön muodon tiettyjen elementtien tuottamisen tai poistaa sen käytöstä käsiteltävien tietojen mukaan. Ne voivat myös keskeyttää asiakirjan luontiprosessin tai näyttää sanomia käyttäjille.)

Voit avata **Kaavojen suunnittelutoiminto** -sivun, kun teet jonkin seuraavista toiminnoista:

- Tietolähteen nimikkeiden sidonta tietomallin komponentteihin
- Tietolähteen nimikkeiden sidonta muotokomponentteihin
- Laskettujen kenttien täydellinen ylläpito tietolähteiden osana
- Käyttäjän syöttöparametrien näkyvyyden ja muokattavauuden ehtojen määritys.
- Käyttäjän syöttöparametrien oletusarvojen määritys.
- Muodon muunnosten rakenne
- Muotokomponenttien ehtojen käyttöönottamisen määritys
- Muodon tiedostokomponenttien tiedostonimien määritys
- Prosessin hallinnan tarkistusten ehtojen määritys
- Prosessin hallinnan tarkistusten sanoman tekstin määritys

## <a name="data-binding"></a><a name="Binding"></a>Tietojen sidonta

ER-kaavojen suunnittelutoiminnon avulla voi määrittää lausekkeen, joka muuntaa tietolähteistä vastaanotetut tiedot niin, että tiedot voidaan täyttää tietojen käyttäjään seuraavalla tavalla suorituksen aikana:

- Sovelluksen tietolähteistä ja suorituksen aikaisista parametreista ER-tietomalliin
- ER-tietomallista ER-muotoon
- Sovelluksen tietolähteistä ja suorituksen aikaisista parametreista ER-muotoon

Seuraavassa kuvassa esitellään tämäntyyppisen lausekkeen rakenne. Tässä esimerkissä lauseke pyöristää **Intrastat.AmountMST**-kentän arvon Intrastat-taulussa kahteen desimaaliin ja palauttaa sitten pyöristetyn arvon.

[![Tietoja sitova lauseke.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Seuraavassa kuvassa esitellään, miten tämän tyyppistä lauseketta voidaan käyttää. Tässä esimerkissä suunnitellun lausekkeen tulos täytetään **Veroraportointimalli**-tietomallin **Transaction.InvoicedAmount**-komponentilla.

[![Tietojen sitovaa lauseketta käytetään.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Suorituksen aikana suunniteltu kaava, `ROUND (Intrastat.AmountMST, 2)` pyöristää kunkin Intrasat-taulun tietueen **AmountMST**-kentän arvon kahteen desimaaliin. Sen jälkeen pyöristetty arvo annetaan **Veroilmoitus**-tietomallin **Transaction.InvoicedAmount**-komponentissa.

## <a name="data-formatting"></a><a name="Transformation"></a>Tietojen muotoilu

ER-kaavojen suunnittelutoiminnon avulla voi määrittää lausekkeen, joka muotoilee tietolähteistä vastaanotetut tiedot niin, että tiedot voidaan lähettää sähköisen asiakirjan luonnin osana. Käytössä voi olla muotoilu, jota on käytettävä tyypillisenä muotoiluna ja jota on käytettävä kaavassa uudelleen. Siinä tapauksessa voit käyttää kyseistä muotoilua kerran muodon määrityksessä nimettynä muunnoksena, jolla on muotoilulauseke. Tämän jälkeen nimetty muunnos voidaan linkittää useisiin muotokomponentteihin, joiden tulosten on oltava luodun muotoilulausekkeen mukaisesti muotoiltuja.

Seuraavassa kuvassa esitellään tämäntyyppisen muotoilun rakenne. Tässä esimerkissä **TrimmedString**-muunnos lyhentää *Merkkijono*-tyyppiset tiedot ja poistamalla ylimääräiset välilyönnit alusta ja lopusta. Se palauttaa sitten lyhennetyn merkkijonon arvon.

[![Muunnos.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Seuraavassa kuvassa esitellään, miten tämäntyyppistä muunnosta voidaan käyttää. Tässä esimerkissä useat muotokomponentit lähettävä tekstin tuloksena suorituksen aikana muodostettavaan sähköiseen asiakirjaan. Kaikki nämä muotokomponentit viittaavat **TrimmedString**-muunnokseen nimellä.

[![Käytettävä muunnos.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kun muodon komponentit, kuten edellisen kuvan **partyName**-komponentti viittaavat **TrimmedString**-muunnokseen, muunnos lähettää tekstin tuotoksena muodostettava sähköiseen asiakirjaan. Tämä teksti ei sisällä edeltäviä eikä lopussa olevia välilyöntejä.

Jos sinulla on muotoiluja, joita tulee kohdistaa yksitellen, voit käyttää muotoilua tietyn muotokomponentin sidonnan yksittäisenä lausekkeena. Seuraavassa kuvassa esitellään tämäntyyppinen lauseke. Tässä esimerkissä **partyType**-muotokomponentti on sidottu tietolähteeseen sen lausekkeen kautta, joka muuntaa saapuvat tiedot tietolähteen **Model.Company.RegistrationType**-kentästä isoilla kirjaimilla kirjoitetuksi tekstiksi. Lauseke lähettää sitten tekstin tuloksena sähköiseen asiakirjaan.

[![Muotoilun käyttö yksittäisessä asiakirjassa.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Prosessinkulun hallinta

ER-kaavojen suunnittelutoimintoa voidaan käyttää määritettäessä lausekkeita, joilla hallitaan muodostettavien sähköisten asiakirjojen prosessinkulkua. Voit suorittaa seuraavat tehtävät:

- Määritä ehdot, jotka määrittävät, milloin asiakirjan luontiprosessi on pysäytettävä.
- Määritä lausekkeet, jotka luovat käyttäjälle sanomia pysäytetyistä prosesseista tai näyttävät suorituslokin sanomia raportin luontiprosessin jatkamisesta.
- Määritä sähköisten asiakirjojen luonnin tiedostonimet ja ohjaa niiden luontiehtoja.

Jokainen prosessinkulun hallinnan sääntö suunnitellaan yksittäiseksi tarkistukseksi. Seuraavassa kuvassa esitellään tämäntyyppinen tarkistus. Tässä on kyseisen esimerkin konfiguraation selitys:

- Tarkistus arvioidaan, kun **INSTAT**-solmu luodaan XML-tiedoston muodostuksen yhteydessä.
- Jos tapahtumaluettelo on tyhjä, tarkistus pysäyttää suoritusprosessin ja palauttaa **EPÄTOSI**-arvon.
- Tarkistus palauttaa virhesanoman otsikolla SYS70894 käyttäjän ensisijaisella kielellä.

[![Valintasäännöt.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER-kaavan luontitoimintoa voidaan käyttää myös sähköisen asiakirjan luonnin tiedostonimen muodostamisessa ja tiedoston luontiprosessin hallinnassa. Seuraavassa kuvassa esitellään tämäntyyppisen prosessikulun hallinnan rakenne. Tässä on kyseisen esimerkin konfiguraation selitys:

- Luettelo **model.Intrastat**-tietolähteen tietueista on jaettu eriin. Kussakin erässä on enintään 1 000 tietuetta.
- Tulos luo zip-tiedoston, joka sisältää yhden XML-muodossa olevan tiedoston jokaisessa luodussa erässä.
- Lauseke palauttaa sähköisen asiakirjan luomiselle tiedostonimen liittämällä tiedostonimen ja tiedostonimen tunnisteen. Toisen erän ja seuraavien erien tiedostonimi sisältää erän tunnuksen loppuliitteenä.
- Lauseke ottaa käyttöön (palauttamalla **TOSI**-arvon) vähintään yhden tietueen sisältävien erien tiedoston luontiprosessin.

[![Prosessinkulun hallinta.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Asiakirjan sisältöohjausobjekti

ER-kaavan suunnittelun avulla voidaan määrittää lausekkeita, jotka ohjaavat, mitä tietoja sijoitetaan luotuihin sähköisiin tiedostoihin suorituksen aikana. Lausekkeet voivat ottaa käyttöön muodon tiettyjen elementtien tuottamisen tai poistaa sen käytöstä käsiteltävien tietojen ja määritetyn logiikan mukaan. Nämä lausekkeet voidaan määrittää yksittäiselle muotoelementille **Toimintojen suunnitteluohjelma** -sivun **Yhdistämismääritykset**-välilehden **Käytössä**-kentässä. Voit kirjoittaa lausekkeet loogiseksi ehdoksi, joka palauttaa *totuusarvon*:

- Jos ehto palauttaa arvon **Tosi**, nykyinen muotoelementti suoritetaan.
- Jos ehto palauttaa arvon **Epätosi**, nykyinen muotoelementti ohitetaan.

Seuraavassa kuvassa esitellään tämäntyyppisiä lausekkeita. (Esimerkkinä käytetään Microsoftin tarjoamaa **ISO20022-siirto (NO)** -muodon kokoonpanon versiota 11.12.11.) **XMLHeader**-muotokomponentti on konfiguroitu kuvaamaan tilisiirtosanoman rakenne ISO 20022 XML -viestistandardien mukaisesti. **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** -muotokomponentti on määritetty lisäämään luotuun viestiin **Ustrd** XML-elementin ja sijoittamaan maksusuoritustiedot ei-rakenteellisessa muodossa tekstinä seuraaviin XML-elementteihin:

- **PaymentNotes**-komponenttia käytetään maksuhuomautusten tekstin luomiseen.
- **DelimitedSequence**-komponentti luo pilkuilla erotetut laskunumerot, joita käytetään nykyisen luottosiirron tilittämiseen.

[![PaymentNotes ja DelimitedSequence -osat.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> **PaymentNotes**- ja **DelimitedSequence** -komponentit merkitään kysymysmerkillä. Kysymysmerkki osoittaa, että komponentin käyttö on ehdollinen. Tässä tapauksessa komponenttien käyttö perustuu seuraaviin kriteereihin:
>
> - `@.PaymentsNotes <> ""`-lauseke, joka on määritetty **PaymentsNotes**-komponentille mahdollistaa (palauttamalla **TOSI**) **Ustrd**-XML-elementin täyttämisen maksuhuomautusten tekstillä, jos nykyisen luottosiirron teksti ei ole tyhjä.
>
>    [![PaymentNotes-komponentin lauseke.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - **DelimitedSequence**-komponentille määritetty `@.PaymentsNotes = ""`-lauseke mahdollistaa (palauttamalla **TOSI**) **Ustrd**-XML-elementin täyttämisen pilkulla erotetuilla laskunumeroilla, joita käytetään nykyisen luottosiirron tilittämiseen, jos maksuhuomautusten teksti tälle luottosiirrolle on tyhjä.
>
>    [![DelimitedSequence-komponentin lauseke.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Tämän asetuksen perusteella kullekin velallisen maksulle luotu **Ustrd**-XML-elementti sisältää joko maksuhuomautusten tekstin tai, kun teksti on tyhjä, tämän maksun tilittämiseen käytetyt pilkulla erotetut laskunumerot.

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Määritettyjen kaavojen oikeellisuustarkistus

Valitse **Kaavansuunnittelija**-sivulla **Testaa** vahvistaaksesi, miten määritetty kaava toimii.

[![Testin valitseminen kaavan tarkistamiseksi.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Kun kaavan argumenttien arvot ovat pakollisia, voit avata **Testaa lauseke** -valintaikkunan **Kaavan suunnittelu** -sivulta. Useimmissa tapauksissa nämä argumentit on määritettävä manuaalisesti, koska määritettyjä sidoksia ei suoriteta suunnittelun aikana. **Kaavansuunnittelija**- sivun **Testi tulos**-välilehdellä näkyy määritetyn kaavan suorituksen tulos.

Seuraava esimerkki osoittaa, miten voit testata ulkomaankaupan toimialueelle määritetyn kaavan ja varmistaa, että Intrastat-kauppatavarakoodi sisältää vain numeroita.

Kun testaat tätä kaavaa, voit käyttää **Testaa lauseke** -valintaikkunaa määrittämään Intrastat-kauppatavarakoodin arvon testausta varten.

[![Intrastat-kauppatavarakoodin määrittäminen testausta varten.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Kun olet määrittänyt Intrastat-kauppatavarakoodin ja valinnut **OK**, **Kaavan suunnittelija** -sivun **testitulos** -välilehdessä näkyy määritetyn kaavan suorituksen tulos. Tämän jälkeen voit arvioida, onko tulos hyväksyttävä. Jos tulosta ei hyväksytä, voit päivittää kaavan ja testata sen uudelleen.

[![Testin tulos.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Joitakin kaavoja ei voi testata suunnittelun aikana. Kaava voi esimerkiksi palauttaa sellaisen tietotyypin tuloksen, jota ei voi näyttää **Testitulos**-välilehdellä. Tässä tapauksessa näyttöön tulee virhesanoma, joka toteaa, että kaavaa ei voi testata.

[![Virhesanoma.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin kaavakieli](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

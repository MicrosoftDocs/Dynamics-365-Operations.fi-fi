---
title: Tuotteen vastaanotto ostotilausten perusteella
description: Tässä ohjeaiheessa käsitellään tuotteiden vastaanotetuiksi rekisteröinnin asetuksia.
author: RichardLuan
manager: tfehr
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, VendPackingSlipJournalListPage, VendPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a07b6b05b8eb25b8c41a5eecbb71fb765a3e9d5f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019676"
---
# <a name="product-receipt-against-purchase-orders"></a>Tuotteen vastaanotto ostotilausten perusteella

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään tuotteiden vastaanotetuiksi rekisteröinnin asetuksia.

Tuotteen vastaanotto on prosessi, joka tallentaa tilatut vastaanotetut tuotteet, jotta ostotilauksen rivit voidaan sitten käsitellä laskutuksessa. Joissakin tapauksissa tuotteet ennakkorekisteröidään, jolloin toimittajan lisätiedot tallennetaan ennen tuotteiden vastaanottoa. Saapuvien tuotteiden tilaksi merkitään ensin **Rekisteröity**. Tuotteiden on sitten ehkä läpäistävä lisäprosesseja, kuten laadun hallintaa, ennen kuin niiden tilaksi merkitään lopuksi **Vastaanotettu**.

## <a name="preregistration-asn"></a>Ennakkorekisteröinti (ASN)
Toimittajat voivat jakaa tietoja tuotteiden lähetysajankohdasta. Tässä tapauksessa voit ennakkorekisteröidä tuotteet tallentamaan nämä tiedot ennen tuotteiden vastaanottoa. Ennakkorekisteröinnin avulla voit vähentää nimikkeen rekisteröinnin ja vastaanoton aikana tehtäviä töitä. Toimittajat voivat antaa tuotetietoja sähköisesti lähetysilmoituksella (ASN), joka kirjataan automaattisesti järjestelmään. ASN-ilmoituksessa on tietoja lähettävien tuotteiden määrästä ja lähetyspäivästä. ASN-ilmoituksella voi olla tietoja esimerkiksi eristä tai sarjanumeroista. ASN-ilmoitus rekisteröidään **Kuljetustenhallinta**-moduulissa.

## <a name="registration"></a>Rekisteröinti
Tuotteen vastaanoton rekisteröinti tehdään varaston saapuvien laiturilla. Se tehdään joko kannettavalla laitteella tai saapumisen kirjauskansioiden avulla. Voit vaihtoehtoisesti rekisteröidä tuotteen vastaanoton manuaalisesti **Rekisteröinti**-toiminnolla **Ostotilaus**-sivulla. Kummassakin tapauksessa tuotteiden tilaksi on merkitty **Rekisteröity**. Huomaa, että tuotteiden tilaksi ei ole vielä merkitty **Vastaanotettu**.  

Varastoon vastaanotettujen tuotteiden on ehkä läpäistävä laatutarkastus ennen niiden poispanoa varastoon. Laatutarkastus voidaan suorittaa laatutilauksilla tai karanteenitilauksilla. Laatutilauksia käytettäessä voit määrittää prosessin estämään tuotteet tilapäisesti varauksen avulla tarkastuksen ajaksi. Karanteenitilauksessa tuotteet siirretään toiseen varastoon tarkastettavaksi. Tätä varastoa kutsutaan karanteenivarastoksi. Kummassakin laaduntarkastusprosessissa osa tuotteista voidaan katsoa hävikiksi, koska ne eivät joko täytä laatuvaatimuksia tai koska laatutarkastukseen sisältyy testaus, jossa otantatuote tuhoutuu.

## <a name="product-receipt"></a>Tuotteen vastaanotto
Useimmiten ostotilauksen tuotteet merkitään **Vastaanotettu**-tilaan käyttämällä **Ostotilaukset**-sivun **Tuotteen vastaanotto** -toimintoa. **Tuotteen vastaanoton kirjaus** -sivulla on useita asetuksia määrän kirjaamiseen vastaanotetuksi. Voit esimerkiksi määrittää **Määrä**-kentän arvoksi **Tilattu määrä** tai **Vastaanottomäärä nyt**. Jos käytössä on varastoon saapumisprosessi, voit vaihtoehtoisesti määrittää tämän kentän arvoksi **Rekisteröity määrä**. Voit muokata kunkin **Vastaanotettu**-tilaan merkittävän tilausrivien määriä mahdollisia poikkeavuuksia vastaaviksi. Kyse voi olla esimerkiksi liian pienestä tai suuresta toimituksesta. Tuotteen vastaanoton yhteydessä on määritettävä tuotteen vastaanoton tunniste, joka viittaa yleensä toimittajan pakkausluetteloon. Tätä tunnistetta tarvitaan kirjanpidossa, sillä sen avulla voidaan tarkistaa vastaanotot toimittajan pakkausluetteloiden perusteella sekä varaston tai kulun laskennan.  

Ostotilauksia voidaan luoda tuotteille, joita ei ole tarkoitettu varastoksi mutta joita pidetään kuluna. Tämä luokka sisältää tilausrivit, jossa varastomalliryhmä on merkinnyt tuotteiden tilaksi **Ei varastoita**, ja hankintaluokkia käyttävät rivit. Tässä tapauksessa nimikkeille ei tehdä varastossa saapumisrekisteröintiä ja vastaanottoa. Sen sijaan **Tuotteen vastaanoton** -toiminto kirjaa vastaanoton suoraan ostotilaukseen ja vastaanotto perustuu tilattuun eikä rekisteröityyn määrään.  

Voit luoda ostotilausrivejä, joissa **Uusi käyttöomaisuus** -vaihtoehto on otettu käyttöön. Tämä vaihtoehto ilmaisee, että ostoa on pidettävä käyttöomaisuutena eikä varastona. Tässä tapauksessa määritetyt käyttöomaisuuden määrityssäännöt määrittävät, ylittääkö tuotteen tai luokan osto tietyt raja-arvot ja onko sitä pidettävänä käyttöomaisuutena, jolloin siinä on käytettävä käyttöomaisuuden hallintaa. Ostoja voidaan tehdä myös aiemmin luodulle käyttöomaisuudelle. Tässä tapauksessa summa oikaistaan tarpeen mukaan.  

Voit valita useita tilauksia ja käsitellä kyseisten tilausten vastaanoton yhdessä. Tätä menetelmää ei käytetä usein, mutta sen käyttöä kannattaa harkita, jos toimittaja on konsolidoinut lähetykset yhdeksi kuormaksi. Kun oston tuote vastaanotetaan, käytössä on toiminto yhteenvetopäivitysten tekemiseen. Yhteenvetopäivityksissä voit kirjata yhden toimittajan pakkausluettelon useisiin ostotilauksiin.  

Ostotilauksia voi luoda myyntitilauksessa, jossa on valittu **Suoratoimitus**-vaihtoehto. Kun suoratoimitusta käytetään, tuotteet eivät saavu koskaan varastoon vaan ne lähetetään suoraan toimittajalta asiakkaalle. Tässä tapauksessa vastaanotto kirjataan yleensä suoraan ostotilaukseen. Vastaanotto voidaan tehdä automaattisesti, esimerkiksi integroimalla sähköinen tiedonsiirto (EDI) toimittajan kanssa. Jos ostotilaus on sen sijaan konsernin sisäinen ostotilaus, Supply Chain Management automatisoi konsernin sisäisen myyntitilauksen vastaanoton lähetyksen yhteydessä. Suoratoimitusta käytettäessä tuotteet lasketaan edelleen varastoksi, vaikka ne eivät fyysisesti saavu varastoon. Kun tuotteen vastaanotto sitten rekisteröidään ostotilaukseen, myyntitilaus päivitetään automaattisesti pakkausluettelolla, jolloin varaston kokonaismuutos on 0 (nolla). Suoratoimitusskenaarioissa ei pidä edellyttää ennakkorekisteröintiä. Jos käytät varastoja, joissa varastonhallinta on otettu käyttöön, voit kiertää rekisterikilven rekisteröintivaatimuksen määrittämällä virtuaalisen varaston. Tämä varasto määritetään tuotteen **Suoratoimituksen varasto** -kentässä. 

Kun tuotteen vastaanotto on käsitelty ostotilauksessa, ostotilauksen tilaksi valitaan **Vastaanotettu**. Se ilmaisee, että tilauksen lasku voidaan käsitellä. Voit tarkastella jo vastaanotettujen tuotteiden tietoja **Tuotteen vastaanoton kirjauskansiot** -sivulla.  

Voit käyttää tätä sivua **Vastaanotto**-toimintoryhmän **Ostotilaus**-sivulla. Kirjauskansiossa on tietoja esimerkiksi määristä, päivämääristä ja dimensioista.

<a name="additional-resources"></a>Lisäresurssit
--------

[Ostotilausten yleiskatsaus](purchase-order-overview.md)

[Ostotilausten luominen](purchase-order-creation.md)

[Ostotilausten hyväksyminen ja vahvistaminen](purchase-order-approval-confirmation.md)

[Toimittajan laskujen yleiskatsaus](../../financials/accounts-payable/vendor-invoices-overview.md)




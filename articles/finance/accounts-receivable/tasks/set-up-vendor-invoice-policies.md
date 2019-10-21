---
title: Määritä toimittajan laskutuskäytännöt
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää toimittajan laskutuskäytännöt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72f017294c976dcd1b7ddda01ac9e39252f036d6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250276"
---
# <a name="set-up-vendor-invoice-policies"></a>Määritä toimittajan laskutuskäytännöt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää toimittajan laskutuskäytännöt. Toimittajan laskukäytännöt suoritetaan, kun toimittajan lasku kirjataan Toimittajan lasku -sivun avulla ja kun Toimittajan laskukäytäntöjen rikkeet -sivu avataan. Voit myös määrittää toimittajan laskun työnkulun, kun haluat suorittaa toimittajan laskukäytännöt aina, kun lasku lähetetään työnkulkuun. 

- Toimittajan laskukäytännöt eivät koske laskurekisteriin tai laskukirjauskansioon luotuja laskuja.  
- Laskun täsmäytyksen vahvistuksessa ei käytetä toimittajan laskukäytäntöjä, vaan Ostoreskontran parametrit -määritettyjä käytäntöjä.  
- Tässä tallenteessa käytetään esittely-yritystä USMF. Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli. Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Toimittajan laskujen käytäntöjen luomisen valmisteleminen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra > Asetukset > Ostoreskontran parametrit**.
2. Valitse **Laskun oikeellisuustarkistus** -välilehti.
3. Valitse **Päivitetäänkö laskun otsikon tila automaattisesti** -valintaruutu tai poista sen valinta.
4. Valitse **OK**.
5. Valitse **Kirjaa lasku, jossa on ristiriitoja** -kentässä vaihtoehto.
6. Sulje sivu.
7. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytännöt**.
8. Valitse **Parametrit**.
9. Valitse **Lisää**.
10. Palaa kotisivulle sulkemalla sivu.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Toimittajan laskujen käytäntösääntöjen tyyppien luominen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytäntösääntöjen tyypit**.
2. Valitse **Uusi**.
3. Kirjoita arvot **Säännön nimi**- ja **Kuvaus**-kenttiin.
4. Avaa haku valitsemalla **Kyselyn nimi**-kentässä avattavan valikon painike ja valitse haluttu tietue.
5. Valitse **Tallenna**.
6. Palaa kotisivulle sulkemalla sivu.

## <a name="define-a-vendor-invoice-policy"></a>Toimittajan laskujen käytännön määrittäminen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytännöt**.
2. Valitse **Uusi**.
3. Kirjoita arvot **Nimi**- ja **Kuvaus**-kenttiin.
4. Laajenna tai tiivistä **Käytännön organisaatiot** -osa.
5. Valitse puussa solmu **Contoso Entertainment System USA**.
6. Valitse **Lisää**.
7. Laajenna tai tiivistä **Käytäntösäännöt**-osa.
8. Valitse **Luo käytäntösääntö**.
9. Kirjoita **Käytäntösäännön kuvaus**-kenttään arvo.
10. Valitse **Suodata**.
11. Valitse **Lisää**. Valitse haluttu tietue.
12. Valitse tai kirjoita kentissä **Taulu**, **Johdettu taulu** ja **Kenttä** arvot avattavista valikoista.
13. Sulje sivu.
14. Kirjoita arvo **Ehdot**-kenttään.
15. Valitse **OK**.
16. Valitse **OK**.
17. Palaa kotisivulle sulkemalla sivut.


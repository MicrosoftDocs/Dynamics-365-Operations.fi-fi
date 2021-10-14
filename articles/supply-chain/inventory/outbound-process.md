---
title: Lähtevien prosessien yleiskuvaus
description: Tässä aiheessa on yleiskatsaus varastonhallinnan lähtevien tuotteiden prosessista.
author: yufeihuang
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 27043828b44cf532d0d8d5091324ba30f3f90cf8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578509"
---
# <a name="outbound-process-overview"></a>Lähtevien prosessien yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä aiheessa on yleiskatsaus varastonhallinnan lähtevien tuotteiden prosessista.

## <a name="output-orders"></a>Toimitustilaukset

Myyntitilausrivit ja siirtotilausrivit linkitetään toimitustilausten avulla lähtevien keräystoimintoihin, jotka käyttävät keräysluetteloita.

Kun keräysluetteloita muodostettaan joko myynti- tai siirtotilauksista, toimitustilaukset ja toimitukset luodaan automaattisesti. Keräysluettelolla on yksi-yhteen-suhde toimitukseen. Siirtotilauksen lähetystä tai myyntitilauksen pakkausluetteloa voi käsitellä lähetyksestä. 

Seuraavassa kaaviossa on yhteenveto toimitustilausten prosessista. 

[![Yhteenveto toimitustilausten prosessista.](./media/outbound-order.png)](./media/outbound-order.png)

Lähtevien sääntöjen avulla voit määrittää, miten ohjelma toteuttaa lähtevien käsittelyn. Voit hallita lähetysprosessia näiden sääntöjen avulla. Näiden sääntöjen avulla voit hallita, mihin prosessin vaiheeseen lähetyksen voi siirtää. Seuraavat asetukset määrittävät, miten lähtevän tavaran prosessit käsitellään.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Myynti- ja siirtotilausten keräilyreitin tila 

Siirry kohtaan **Myyntireskontra** \> **Asetukset** \> **Myyntireskontran parametrit** ja valitse sitten **Päivitykset**-välilehdellä arvo **Keräilyreitin tila** -kenttään.

[![Myyntitilausten keräilyreitin tila -kenttä.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Jos **Keräilyreitin tila** -kentän arvoksi on asetettu **Valmis**, keräilyprosessi toteutetaan automaattisesti keräysluettelon muodostamisprosessin osana. Jos kentän arvo on **Aktivoitu**, keräysluettelon rivit on päivitettävä manuaalisesti.

Samat asetukset koskevat siirtotilauksia. Siirry kohtaa **Varastonhallinta** \> **Asetukset** \> **Varasto ja varastonhallinnan parametrit**, ja valitse sitten **Kuljetus**-välilehden **Keräilyreitin tila** -kenttään arvo.

[![Siirtotilausten keräilyreitin tila -kenttä.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Toimitustilausten lopettaminen

Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Varasto ja varastonhallinnan parametrit**, ja valitse sitten **Yleiset**-välilehden **Lopeta toimitustilaus**-vaihtoehto.

[![Lopeta toimitustilaus -vaihtoehto.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Kun varastotyöntekijä vähentää keräysluettelon määriä, vastaavat varastotilauksen määrät poistetaan lähetyksestä. Kun keräysluettelo päivitetään tiettynä ajankohtana, jäljellä olevat määrät raportoidaan takaisin tilaukseen, jos **Lopeta toimitustilaus** -asetukseksi on määritetty **Kyllä**. Jos **Lopeta toimitustilaus** -asetukseksi on määritetty **Ei**, jäljellä olevat määrät säilytetään avoimen toimitustilauksen määränä. Ne on lisättävä uuteen keräysluetteloon **Avoimet toimitustilaukset** -toiminnon osana. 

[![Avoimet toimitustilaukset -komento Toiminnot-valikossa.](./media/open-output-order.png)](./media/open-output-order.png)

[![Toiminnot-valikko Avoimet toimitustilaukset -sivulla.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Vähennä määrää

Keräysluetteloiden muodostamisprosessissa voi käyttää myös kolmatta parametria, **Vähennä määrää**. Tämän parametrin asetus toimii yhdessä **Varaus**-asetuksen kanssa, joka käynnistää varausprosessin osana varastoon vapauttamista.

[![Vähennä määrää -parametri.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Esimerkki myyntitilauksen lähtevästä prosessista

Tässä esimerkissä on kaksi nimikettä sisältävä myyntitilaus. Valitse keräysluettelon luonnin aikana **Vähennä määrää** -parametri. Siksi keräysrivejä vapautetaan ja luodaan ainoastaan käytettävissä olevalle varastolle. Keräily on raportoitava keräysluetteloiden rekisteröintiprosessin kautta (**Keräilyreitin tila** = **Aktivoitu**).

Varasto, jota ei ole vielä varattu, varataan keräysluettelon luonnin aikana. Ei käytettävissä olevan varaston voi joko poistaa myyntitilaukselta tai vapauttaa varastoon myöhempää käsittelyä varten, kun varasto on käytettävissä keräilyyn.

[![Päivitä keräysluettelo.](./media/update-picking-list.png)](./media/update-picking-list.png)

Kun kaikki **Keräysluettelon kirjaaminen** -sivun keräilyrivit on kerätty, liittyvä lähetys on valmis. Myyntitilausten pakkausluetteloprosessi voidaan sitten alustaa keräillyn varaston perusteella.

[![Lähtevien lähetysten päivittäminen.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
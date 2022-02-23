---
title: BOPIS:n määrittäminen Dynamics 365 Commerce -arviointiympäristössä
description: Tässä ohjeaiheessa selitetään, miten BOPIS (osta verkosta, nouda myymälästä) määritetään Microsoft Dynamics 365 Commerce -arviointiympäristössä, kun se on valmisteltu.
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 62dabaa2610341cc8ad8e85812a317ac3123fcb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411868"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a>BOPIS:n määrittäminen Dynamics 365 Commerce -arviointiympäristössä

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa selitetään, miten BOPIS (osta verkosta, nouda myymälästä) määritetään Microsoft Dynamics 365 Commerce -arviointiympäristössä, kun ympäristö on valmisteltu.

## <a name="prerequisite"></a>Edellytys

Suorita tämän ohjeaiheen toimet vasta, kun Commercen arviointiympäristö on valmisteltu ja määritetty. Lisätietoja ympäristön valmistelusta ja määrittämisestä on kohdissa [Dynamics 365 Commerce -arviointiympäristön valmisteleminen](provisioning-guide.md) ja [Dynamics 365 Commerce -arviointiympäristön määrittäminen](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).

Kun Commerce-ympäristö on valmisteltu ja määritetty päättyneeksi, voit ottaa käyttöön BOPIS-skenaariot tämän ohjeaiheen avulla.

## <a name="configure-the-pos"></a>Määritä POS

### <a name="configure-modern-pos"></a>Modern POS:in määrittäminen

BOPIS-skenaariot, joihin liittyy luottokorttimaksu, edellyttävät laitteistoasemaa. Laiteasema muodostetaan Windowsin Modern POS:iin Windowsille ja Androidille. Jos käytät iOS POS-tai Modern POS-sovellusta iOS:lle, myyntipisteasiakasohjelman on muodostettava laitepari jaetun laiteaseman kanssa. Tässä ohjeaiheessa selitetään, kuinka BOPIS määritetään Windows- ja Android-asiakkaita varten. Lisätietoja jaetun laiteaseman asentamisesta on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> POS-asetukset \> Kassakoneet**.
2. Valitse rekisteröi **SANFRAN-5** ja valitse sitten **Muokkaa**.
3. Muuta **laitteistoprofiili**-kentän arvo **HW002**-arvosta **HW001**-arvoon ja valitse sitten **Tallenna**.
4. Synkronoidaksesi muutokset, siirry kohtaan **Retail ja Commerce \> Retail ja Commercen IT \> Jakeluaikataulu**.
5. Valitse jakeluaikataulu **1090** ja valitse sitten toimintoruudusta **Suorita nyt**.
6. Valitse **Kyllä** ja aloita tietojen synkronointi valitsemalla **OK**. 

### <a name="install-modern-pos"></a>Asenna Modern POS

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> Laitteet**.
2. Valitse laite **SANFRANCIS-5**.
3. Valitse toimintoruudussa **Lataa** ja valitse sitten **määritystiedosto**.
4. Valitse **Lataa** ja valitse sitten **Retail Modern POS**. 
5. Kun **ModernPOSSetup.exe**-tiedoston lataus on päättynyt, valitse **Avaa tiedosto**.

    ![Avaa tiedosto](./dev-itpro/media/PAYMENTS/openfile.png)

6. Valitse **Seuraava**, jos haluat käydä läpi asennusprosessin. Kun asennus on päättynyt, valitse **Sulje**.

### <a name="activate-modern-pos"></a>Modern POS -toiminnon aktivoiminen

1. Valitse Windowsin työpöydällä **Käynnistä**-painike ja syötä **Retail Modern POS**.
2. Valitse **Retail Modern POS** -sovellus, jonka aktivointi aloitetaan.
3. Valitse **Seuraava**. **Palvelimen URL-osoite**, **laitetunnus** ja **rekisterinumero**-kentät on määritettävä valmiiksi käyttämällä edellisessä kohdassa lataamaasi määritystiedoston tietoja.
4. Valitse **Aktivoi**.
5. Näyttöön tulee todennusvalintaikkuna. Valitse tili, joka käyttää sähköpostiosoitetta, joka yhdistettiin aiemmin työntekijään **000713 - Andrew Collette**.

    > [!NOTE]
    > Jos et ole vielä liittänyt työntekijää henkilöllisyytesi, aktivointi epäonnistuu. Noudata tässä tapauksessa Liitä työntekijä henkilöllisyyteesi -kohdan ohjeita ohjeaiheessa [Määritä Dynamics 365 Commerce -arviointiympäristö](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
6. Kun sinua kehotetaan antamaan organisaatiosi hallita laitetta, valitse **Vain tämä sovellus**.
7. Kun aktivointi on tehty, valitse **Aloita**.

### <a name="enable-bopis-in-modern-pos"></a>Ota käyttöön BOPIS Modern POS:issa

1. Kirjaudu sisään Modern POS-sovellukseen käyttämällä **000713** -operaattoritunnusta ja **123**-salasanaa.
2. Kun videota toistetaan, valitse kaksi valintaruutua valintaikkunan vasemmassa alakulmassa ja sulje valintaikkuna.
3. Jos sinua ei kehoteta sulkemaan vaihtonäppäintä, siirry **Aloitus**-sivulla oikealle, valitse **Sulje vaihto** ja kirjaudu sitten takaisin POS-sovellukseen.
4. Kun olet kirjautunut sisään, valitse **Suorita muu kuin kassatoiminto**, kun sinua kehotetaan tekemään niin.
5. Siirry **Aloitus**-sivulla oikealle ja valitse **Valitse laiteasema** -toiminto.
6. Valitse **Hallitse**, määritä **Käytä laiteasemaa** -asetukseksi **Käytössä** ja valitse sitten **OK**.
7. Kirjaudu ulos myyntipisteestä ja kirjaudu takaisin sisään.
8. Kun olet kirjautunut sisään, valitse **Avaa uusi vaihto** ja valitse sitten **Kassa**.

## <a name="complete-a-bopis-scenario"></a>Suorita BOPIS-skenaario loppuun

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Luo myymälätilaus noutomyymälälle

1. Siirry sen URL-osoitteen kohdalle, jonka määritit [Alusta e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) -vaiheessa ympäristön määrityksen aikana.
2. Valitse nimike ja valitse **Lisää ostoskoriin**.
3. Valitse ostoskassisivulla juuri lisäämäsi tilausrivin **Nouto**.
4. Kirjoita **Valitse myymälä** -valintaikkunaan **San Francisco** ja valitse sitten **Haku**-painike.
5. Etsi tulosluettelosta San Franciscon liike ja valitse **nouto tästä**.
6. Valitse ostoskassisivulta **Kassalle vieraana**. 

    > [!NOTE]
    > Jos haluat jatkaa kassalle, sinun on hyväksyttävä evästeilmoitus. Tämä ilmoitus näkyy bannerissa Kassa-sivun yläosassa.

7. Kirjoita luottokortin maksutapakenttään seuraavat tiedot:

    - **Kortinhaltijan nimi:** Syötä mikä tahansa nimi.
    - **Kortin numero:** Syötä **4111-1111-1111-1111**.
    - **Vanhentumispäivä:** Syötä **10/20**.
    - **Kortin tarkistusnumero (CVV) -koodi:** Syötä **737**.

    > [!IMPORTANT]
    > Älä milloinkaan, missään tapauksessa yritä käyttää testisivustossa todellisia luottokortin tietoja.

8. Jatka kassalle syöttämällä laskutusosoitteen tiedot ja valitse sitten **Tallenna ja jatka**.
9. Kun tilaus on valmis lähetettäväksi, valitse **Kassa**.

### <a name="synchronize-online-orders-to-the-back-office"></a>Online-tilausten synkronoiminen taustajärjestelmään

Tietoja online-tilausten synkronoimista on kohdassa [Online-myynnin ja -maksujen kirjaaminen](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).

### <a name="pick-up-an-order-in-the-store"></a>Nouda tilaus myymälästä

1. Kirjaudu myyntipisteeseen.
2. Valitse **Aloitus**-näytössä **Tilauksen täyttäminen**
3. Valitse noudettavien nimikkeiden luettelosta rivi, joka on sijoitettu online-tilassa olevaan tilaukseen.
4. Kun tilausrivi on valittuna, valitse **Nouda**.

    Rivinimike lisätään transaktionäyttöön ja **$0,00** näkyy erääntyvänä saldona.

5. Valitse saldo, jonka määrä on **$0,00**, tai valitse mikä tahansa maksutapa transaktion tekemistä varten.

## <a name="troubleshooting"></a>Vianmääritys

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>POS:ista noudettavien online-tilausten saldo ei ole nolla

Jos erääntyvä saldo ei ole 0 (nolla), kun tilaus haetaan myymälässä tapahtuvaa noutoa varten, varmista, että käytössä on Modern POS ja että laitteistoasema on aktiivinen. Jos käytössä on Cloud POS tai iOS:n Modern POS, varmista, että jaettu laiteasema on aktiivinen. Online-tilassa suoritettavien maksujen noutamiseen tarvitaan jonkinlaista aktiivista laiteasemaa.

### <a name="general-issues-with-payment-capture"></a>Maksun tarkistukseen liittyvät yleiset ongelmat

Kaikkien yleisten ongelmien varalta kannattaa aina tutustua Modern POS- tai Internet Information Services (IIS) -laiteasemien tapahtumalokeihin. Nämä lokit löytyvät Windowsin tapahtumalokin seuraavista solmuista:

- Sovellus- ja palvelulokit \> Microsoft \> Dynamics \> Commerce-ModernPOS
- Sovellus- ja palvelulokit \> Microsoft \> Dynamics \> Commerce-laiteasema

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commerce -arviointiympäristön yleiskuvaus](cpe-overview.md)

[Dynamics 365 Commerce -arviointiympäristön valmisteleminen](provisioning-guide.md)

[Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset](cpe-optional-features.md)

[Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)

[Adyen-maksuyhdistin](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[Online-maksuvälineiden tallentaminen Adyen-yhdistimen avulla](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[Omnikanavamaksujen yleiskatsaus](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)

---
title: BOPIS:n määritykset Dynamics 365 Commercen eristysympäristössä
description: Tässä artikkelissa selitetään, miten osta verkosta, nouda myymälästä (BOPIS) määritetään Microsoft Dynamics 365 Commercen eristysympäristössä, kun se on valmisteltu.
author: BrianShook
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16cea7beb6ca05b5e96a9713b1217b414e27d56e
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013159"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-sandbox-environment"></a>BOPIS:n määritykset Dynamics 365 Commercen eristysympäristössä

[!include [banner](includes/banner.md)]

Tässä artikkelissa selitetään, miten osta verkosta, nouda myymälästä (BOPIS) määritetään Microsoft Dynamics 365 Commercen eristysympäristössä, kun ympäristö on valmisteltu.

## <a name="prerequisite"></a>Edellytys

Suorita tämän artikkelin toimet vasta, kun Commercen eristysympäristö on valmisteltu ja määritetty. Katso lisätietoja Commercen eristysympäristön valmistelusta ja määrittelystä kohdasta [Dynamics 365 Commercen eristysympäristön valmisteleminen](provisioning-guide.md) ja [Dynamics 365 Commercen eristysympäristön määrittäminen](./cpe-post-provisioning.md).

Kun Commerce-ympäristö on valmisteltu ja määritetty päättyneeksi, voit ottaa käyttöön BOPIS-skenaariot tämän artikkelin avulla.

## <a name="configure-the-pos"></a>Määritä POS

### <a name="configure-modern-pos"></a>Modern POS:in määrittäminen

BOPIS-skenaariot, joihin liittyy luottokorttimaksu, edellyttävät laitteistoasemaa. Laiteasema muodostetaan Windowsin Modern POS:iin Windowsille ja Androidille. Jos käytät iOS POS-tai Modern POS-sovellusta iOS:lle, myyntipisteasiakasohjelman on muodostettava laitepari jaetun laiteaseman kanssa. Tässä artikkelissa selitetään, kuinka BOPIS määritetään Windows- ja Android-asiakkaita varten. Lisätietoja jaetun laiteaseman asentamisesta on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](./retail-hardware-station-configuration-installation.md).

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

    ![Avaa tiedosto.](./dev-itpro/media/PAYMENTS/openfile.png)

6. Valitse **Seuraava**, jos haluat käydä läpi asennusprosessin. Kun asennus on päättynyt, valitse **Sulje**.

### <a name="activate-modern-pos"></a>Modern POS -toiminnon aktivoiminen

1. Valitse Windowsin työpöydällä **Käynnistä**-painike ja syötä **Retail Modern POS**.
2. Valitse **Retail Modern POS** -sovellus, jonka aktivointi aloitetaan.
3. Valitse **Seuraava**. **Palvelimen URL-osoite**, **laitetunnus** ja **rekisterinumero**-kentät on määritettävä valmiiksi käyttämällä edellisessä kohdassa lataamaasi määritystiedoston tietoja.
4. Valitse **Aktivoi**.
5. Näyttöön tulee todennusvalintaikkuna. Valitse tili, joka käyttää sähköpostiosoitetta, joka yhdistettiin aiemmin työntekijään **000713 - Andrew Collette**.

    > [!NOTE]
    > Jos et ole vielä liittänyt työntekijää henkilöllisyytesi, aktivointi epäonnistuu. Noudata tässä tapauksessa Liitä työntekijä henkilöllisyyteesi -kohdan ohjeita artikkelissa [Määritä Dynamics 365 Commercen eristysympäristö](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
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

1. Siirry sen URL-osoitteen kohdalle, jonka määritit [Alusta e-Commerce](./provisioning-guide.md#initialize-e-commerce) -vaiheessa ympäristön määrityksen aikana.
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

Tietoja online-tilausten synkronoimista on kohdassa [Online-myynnin ja -maksujen kirjaaminen](./tasks/posting-online-sales-payments.md).

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

[Dynamics 365 Commercen eristysympäristön valmistelu](provisioning-guide.md)

[Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen eristysympäristöä varten](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)

[Adyen-maksuyhdistin](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[Online-maksuvälineiden tallentaminen Adyen-yhdistimen avulla](./dev-itpro/adyen-connector-listpi.md)

[Omnikanavamaksujen yleiskatsaus](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

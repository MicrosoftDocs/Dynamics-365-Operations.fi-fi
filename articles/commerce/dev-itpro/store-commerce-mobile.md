---
title: Store Commerce ‑sovellus mobiiliympäristöille
description: Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Commerce Store Commerce -sovelluksen käyttäminen aloitetaan Android- ja iOS-laitteessa.
author: stuharg
ms.date: 11/30/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: dc952698a2a3301aff312e8310c58cbbb9cfe290
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815780"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Store Commerce ‑sovellus mobiiliympäristöille

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Commerce Store Commerce -sovellusten käyttäminen aloitetaan Android- ja iOS-laitteessa.

Dynamics 365 Commerce -mobiilisovelluksissa Android- ja iOS-laitteita varten otetaan käyttöön mobiililaitteen myyntipistelaitteet jälleenmyyntiympäristöä varten suoraviivaisesti ja yksinkertaisesti. Store Commerce -mobiilisovellukset tarjoavat lähes kaikki samat ominaisuudet ja edut kuin [Store Commerce -sovellus Windowsille](store-commerce.md), ja ne toimivat hyvin erilaisissa iOS- ja Android-puhelimissa ja -tableteissa. Store Commerce -mobiilisovellukset voidaan asentaa suoraan Apple- ja Google Play -sovelluskaupoista. Kehittäjän ei tarvitse luoda uutta sovelluspakettia niiden käyttöönottamista tai päivittämistä varten. 

Store Commerce -mobiilisovellukset säilyttävät täydellisen toiminnallisen pariteetin nykyisten Retail-hybridisovellusten kanssa. Lisäksi Store Commerce for iOS sisältää määritetyn laiteaseman tuen, jotta iOS-laitteet voivat olla yhteydessä verkossa olevien maksupäätteiden, kuittitulostimien ja kassojen kanssa ilman jaetun laiteaseman käyttöönottoa. 

> [!IMPORTANT]
> Store Commerce -sovellukset Windowsille, Android ja iOS ovat Dynamics 365 Commercen myyntipistesovellusten seuraava sukupolvi. Store Commerce -sovellukset tarjoavat lukuisia parannuksia verrattuna edeltäjiinsä. Samalla niissä on samat toiminnot ja ominaisuudet. Microsoft poistaa MPOS:n sekä Android- ja iOS Retail POS -hybridisovellukset loppuvuodesta 2023 ja suosittelee Store Commercen tai Cloud POS:n (CPOS) käyttämistä kaikissa uusissa POS-käyttöönotoissa. Olemassa olevien asiakkaiden tulisi suunnitella siirtyminen Retail-hybridisovelluksista Store Commerce -sovellukseen. Lisätietoja: [Siirry Modern POS -sovelluksesta Store Commerceen](pos-extension/migrate-mpos-store-commerce.md). 

## <a name="app-architecture"></a>Sovellusarkkitehtuuri

Store Commerce -mobiilisovellukset käyttävät samaa topologiaa kuin Store Commerce -sovellus Windowsille, kun se otetaan käyttöön hybriditilassa. Store Commerce -mobiilisovellukset ovat liittymäsovelluksia, jotka hahmontavat CPOS:n suoraan Commerce Scale Unitista (CSU) ja yhdistävät sen päätelaitteettomaan kaupankäyntiin ja Commerce headquartersiin CSU:n kautta. Liittymäsovelluksen avulla Store Commerce -sovellukset tukevat määritettyä laiteasemaa suorassa integroinnissa maksupäätteen, tulostimen, kassan ja muiden oheislaitteiden kanssa. Sinun ei tarvitse määrittää jaettua laiteasemaa laitteiston käyttämiseksi. 

Jos haluat päivittää Store Commerce -mobiilisovelluksen, sinun on päivitettävä ainoastaan CSU. Sovellus noutaa automaattisesti kaikki uudet myyntipistetoiminnot ja -ominaisuudet. Lisätietoja CSU:n päivittämisestä on kohdassa [Commerce Scale Unitin (pilviversio) päivitysten ja laajennusten kohdistaminen](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

Liittymäsovellukset huolletaan sovelluskaupan päivitysten kautta. Kun aliversio saavuttaa yleisen saatavuuden, Microsoft julkaisee sen sovelluskaupoissa. Microsoft saattaa myös julkaista korjaustiedostoja aliversion päivitysten välillä korkean prioriteetin korjaustiedostojen julkaisemista varten.

## <a name="prerequisites"></a>Edellytykset

Store Commerce -mobiilisovellukset vaativat Dynamics 365 Commercen erityisesti Commerce headquarters- ja CSU-komponentteja varten. Seuraavassa taulukossa on lueteltu käyttöjärjestelmän ja CSU:n vähimmäisversiot, jotka Android- ja iOS-mobiilisovellukset edellyttävät. 

| Edellytys | Android      | iOS  |
| ------------ | ------------ | ---- |
| Käyttöjärjestelmäversio   | 7.0          | 15.0 |
| CSU-versio  | 9.38.22266.8 | Päätetään myöhemmin  |

## <a name="install-the-app"></a>Sovelluksen asentaminen

Voit asentaa Store Commerce -mobiilisovellukset suoraan Google Play -kaupasta tai Apple App Storesta. 

- [Store Commerce -sovellus Androidille](https://aka.ms/storecommerceandroid)
- [Store Commerce -sovellus iOS:lle](https://aka.ms/storecommerceios)

Android-sovellus (.apk) ja Apple-sovellus (.ipa) -paketit voidaan pian ladata Microsoft Dynamics Lifecycle Servicesin Jaettu omaisuuskirjasto -kohdassa. 

## <a name="device-and-register-setup"></a>Laitteen ja kassan asetukset

Ennen kassan aktivoimista Store Commerce -mobiilisovelluksissa on määritettävä laite ja kassa Commerce headquartersissa. Lisätietoja on kohdassa [Laitteet ja kassat](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Laitteen asetukset

Näiden ohjeiden avulla voit luoda ja määrittää uuden laitteen.

1. Siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Kanavan asetukset \> Myyntipisteen asetukset \> Laitteet**. 
1. Luo uusi laite ja valitse sovellustyypiksi **Modern POS - Android** tai **Modern POS - iOS** riippuen käyttöönotettavasta mobiilisovelluksesta. 

    > [!NOTE] 
    > **Modern POS - Android**- ja **Modern POS - iOS** -sovellustyyppejä käytetään myös nykyisten hybridisovellusten käyttöönotossa Android- ja iOS-laitteissa. MPOS:n vanhenemisen jälkeen näiden sovellustyyppien etiketeiksi päivitetään **Store Commerce - Android** ja **Modern POS - iOS**. 

### <a name="register-setup"></a>Kassakoneen asetukset

Voit luoda uuden kassan ja liittää sen luomaasi laitteeseen tai vaihtoehtoisesti voit liittää olemassa olevan kassan uuteen laitteeseesi. Lisätietoja kassoista on kohdassa [Kassojen luominen ja liittäminen](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Näyttöasettelun asetukset

Jos määrität uudelleen näyttöasettelua, joka sisällytettiin Dynamics 365 Commerce -käyttöoikeuden esittelytietoihin, Store Commerce -sovellus valitsee automaattisesti kompaktin asettelun, jos laitteen näytön tarkkuus on pienempi kuin 480 &times; 853 kuvapistettä pystysuunnassa. Jos kuitenkin olet luomassa näyttöasettelua alusta alkaen tai jos kannettavan laitteen tarkkuus on suurempi kuin kompaktin asettelun tukema tarkkuus, varmista, että luot tarkkuuden ja liittyvät painikeruudukot niin, että ne sopivat käytettävälle puhelimelle tai tabletille. Lisätietoja näytön asettelun määrityksistä on kohdassa [Myyntipisteen käyttöliittymän visuaaliset määritykset](../pos-screen-layouts.md). 

Kun laitteet ja kassat on määritetty, siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Retail ja Commerce -tunnus \> Jakeluaikataulut** ja suorita kassojen työ.

## <a name="activate-a-device"></a>Laitteen aktivoiminen

Voit aktivoida laitteen Store Commerce -mobiilisovelluksessa noudattamalla seuraavia ohjeita.

1. Avaa sovellus mobiililaitteessa.
1. Syötä CPOS-URL-osoite, joka löytyy ympäristön tietojen sivulta Lifecycle Services -ratkaisussa sekä Commerce headquartersin **Kanavan profiilit** -sivulta (**Retail ja Commerce \> Kanavan asetukset \> Kanavan profiilit**).
1. Kirjaudu sisään käyttämällä sen työntekijän tunnistetietoja, jolla on käyttöoikeudet laitteiden hallintaan.
1. Valitse myymälä, joka on liitetty Commerce headquartersissa luomaasi tai uudelleenkäyttämääsi kassaan.
1. Valitse kassa, joka on liitetty Commerce headquartersissa luomaasi tai uudelleenkäyttämääsi laitteeseen.
1. Laite tulee nyt aktivoida. Voit kirjautua sisään kassaan käyttämällä valitsemaasi myymälään liitetyn työntekijän operaattorin tunnusta ja salasanaa. 

Lisätietoja laitteen aktivoinnista on kohdassa [Myyntipisteen laitteen aktivoiminen](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Ominaisuuden pariteetti Store Commerce Windowsille -sovelluksen kanssa

Seuraavassa taulukossa vertaillaan Store Commerce -sovelluksen ominaisuuksia Windows-, Android- ja iOS-ympäristöissä.

| Ominaisuus                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Varattu laiteasema                                                            | Kyllä     | Kyllä     | Kyllä |
| Jaettu laiteasema                                                               | Kyllä     | Kyllä     | Kyllä |
| Tietoliikenne verkossa olevien oheislaitteiden (maksupääte, tulostin ja kassa) kanssa | Kyllä     | Kyllä     | Kyllä |
| OLE for Point of Sale (OPOS) -oheislaitteet paikallisessa laiteasemassa             | Kyllä     | En      | En  |
| Offline-tila                                                                          | Kyllä     | En      | En  |

## <a name="additional-resources"></a>Lisäresurssit

[Store Commerce -sovellus](store-commerce.md)

[Valitse Store Commerce tai Cloud POS](../mpos-or-cpos.md)

[Store Commercen määritys- ja asennusongelmien vianmääritys](../troubleshoot/store-commerce-setup-installation.md)

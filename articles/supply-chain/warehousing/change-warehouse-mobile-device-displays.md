---
title: "Varaston mobiililaitteen näyttöasetukset"
description: "Tässä artikkelissa kuvataan mobiililaitteen näytön ulkoasun määrittämistä ja kuinka pikanäppäimet yhdistetään ohjaimiin, kuten painikkeisiin."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 799cd4a940813e39f8be6b4c127b9efabc88e909
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-mobile-device-display-settings"></a>Varaston mobiililaitteen näyttöasetukset

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan mobiililaitteen näytön ulkoasun määrittämistä ja kuinka pikanäppäimet yhdistetään ohjaimiin, kuten painikkeisiin. 

Tämä artikkeli koskee "erikoisvarastointikäyttö"-ominaisuuksia Varastonhallinnassa. Mobiililaitteita voidaan käyttää moniin tehtäviin, joita varastotyöntekijät suorittavat.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Määritä tyylit ja yhdistä pikanäppäimet
Osana mobiililaitteen konfigurointia voit määrittää mobiililaitteille erilaisia asetteluja. Jos haluat tehdä tämän, sinun on tiedettävä CSS-tiedoston ja ASPX-tiedoston nimet. Oletustiedostot on asennettu osana varaston mobiililaiteportaalin asennusta. Jos et tiedä tiedostonimiä, kysy järjestelmänvalvojalta. Voit määrittää uuden tyylin **Mobiililaitteen näyttöasetukset** -sivulla:

-    Syötä **CSS-tiedosto**-kenttään CSS-tiedostosi nimi. Sisällytä nimeen .css tiedostonimen tunniste.
-   Määritä **Mobiililaitteen näyttöasetusten näkymä** -sivulla ASPX-tiedosto: **Älä** sisällytä .aspx tiedostonimen tunnistetta.

CSS- ja ASPX-tiedostojen on sijaittava tietyssä hakemistossa niin, että Internet Information Services (IIS) -sovellus pystyy lataamaan ne. Voi olla hyvä ajatus määrittää eri CSS-tiedostot, jos käytät mobiililaitetoimintoa eri selaimissa tai erityyppisillä laitteilla, jotka vaativat erilaista asettelunhallintaa. Yksinkertaisia asetuksia kuten taustaväriä, tekstifonttia ja fontin väriä, sekä painikkeiden leveyttä ja toimintaa, voidaan hallita helposti erilaisella CSS-tiedostojen käytöllä. ASPX-tiedostoa käytetään näyttämään mobiilisivusto palvelinpuolen ASP.NET-sovelluksessa. Tämä tiedosto hallitsee sitä, miten HTML:n yleisrakenne on aseteltu. Tätä toimintoa tulisi mukauttaa vain, jos sinulla on vakavia rakenteellisia ongelmia HTML:n ja JavaScriptin kanssa ja joudut muuttamaan tämän koodin tietyille laitteillesi. Yhdistä mobiililaitteen sivun HTML-ohjausobjektit pikanäppäimiin **Mobiililaitteen näyttöasetukset** -sivun **Pikanäppäin**-kentässä määrittämällä näppäimille numeeriset koodit. Löydät numerokoodit mobiililaitteen **Näytä pikanäppäinten koodit** -valikosta. Huomioi, että yhdistämismääritykset saattavat olla erilaiset käytetystä laitteesta riippuen. Sinun on käytettävää seuraavaa syntaksia yhdistämisen luomiseksi:

&lt;control name&gt;(&lt;key name&gt;)=&lt;key code&gt;;

Alla on kuvaus syntaksin osista:

-   **&lt;control name&gt;**>: HTML-muodossa hahmonnetun ohjausobjektin, kuten painikkeen, nimi.
-   **(&lt;key name&gt;)** – Sen näppäimistönäppäimen nimi, jolle luot pikanäppäimen.
-   **&lt;Key code&gt;** – Pikanäppäimenä käytettävän näppäimen numerokoodi.

Tässä on esimerkki:

Peruuta(Esc)=27; Kokonaan(F2)=113

Kaikilla sivuilla, jotka sisältävät **Peruuta**-painikkeen, painikkeessa näkyy tämä teksti:

**(Esc) Peruuta**

Näppäimistön Esc-näppäin aktivoi **Peruuta**-painikkeen. Jos haluat käyttää tyyli- ja pikanäppäinasetuksia tietyllä laitteella, sinun on luotava yhdistämismääritys **Ehdot**-kentässä. Sinun on käytettävä .NET säännönmukaista lauseketta yhdistämisen luontiin, ja lausekkeen on koostuttava kolmesta pystyviivalla (|) erotetusta osasta alla olevan mukaisesti:

Request.UserHostAddress=&lt;user host address&gt;|HostName=&lt;user host name&gt;|Request.UserAgent=&lt;user agent&gt;

Alla on kuvaus lausekkeen osista:

-   **&lt;user host address&gt;** – Säännönmukainen .NET-lauseke, joka vastaa pyytäjän IP-osoitetta.
-   **&lt;user host name&gt;** – Säännönmukainen .NET-lauseke, joka vastaa pyytäjän verkon nimeä.
-   **&lt;user agent&gt;** – Säännönmukainen .NET-lauseke, joka vastaa pyytäjän käyttämän selaimen tunnusta.

Seuraava esimerkki mahdollistaa Internet Explorer 8:n käytön.

Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0

Löydät tietoa asetuksista mobiililaitteen **Näytä näyttöasetusten palvelinkonfiguraatio** -valikosta.

## <a name="define-text-colors-for-messages"></a>Mobiililaitteiden tekstin värien määrittäminen
Hallinnoi järjestelmän luomien sanomien käyttämien, kuten virhesanomien, värejä **Mobiililaitteen tekstin värit** -sivulla. Tekstin väri voi esimerkiksi ilmaista sanoman tarkoitusta tai vakavuutta. Seuraavat sanomatyypit näytetään.

| Sanomalaji | Kuvaus                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Oletusarvo      | Oletussanomat käyttävät oletusmuotoisia väriasetuksia, jotka on määritetty varaston mobiililaiteportaalin CSS-tiedostossa.                                                   |
| Virhe        | Virhesanomat ilmaisevat ongelman, joka käyttäjän on ratkaistava ennen kuin hän voi jatkaa.                                                                                             |
| Onnistui      | Onnistumissanomat vahvistavat että toiminto onnistui.                                                                                                                                |
| Varoitus      | Varoitussanomat ilmoittavat työntekijälle ongelmasta tai mahdollisesta ongelmasta, jos työntekijä jatkaa. Työntekijän ei kuitenkaan tarvitse ratkaista ongelmaa jatkaakseen. |

Valitse väri **Valitse väri** -sivulla napsauttamalla värivalikoimaa tai kirjoittamalla heksadesimaalin värikoodi.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Määritä mobiililaitteissa käytettävä päivämäärämuoto
Voit laajentaa hyväksyttyjä päivämäärän esitysmuotoja jokaisessa asennuksessa. Tämä ominaisuus voi olla hyödyllinen, jos esimerkiksi haluat tarjota muodon, joka tekee työntekijälle päivämäärien kirjoittamisen helpommaksi mobiililaitteella. Oletusmuodon määrää käyttäjän oletuskieli, joka on määritetty **Käyttäjän asetukset** -sivun **Kieli**-kentässä. (Samalla sivulla on käytössä myös työntekijän liittäminen tiettyyn varaston työn käyttäjään.) **Huomautus:** Varaston mobiililaiteportaali ei käytä **Päivämäärä-, kellonaika- ja numeromuoto** -kentän asetusta **Kieli- ja alueasetukset** -sivulla. Jotta voit muuttaa päivämäärän muotoa, sinun on tunnettava Microsoft .NET Frameworkin säännönmukaiset lausekkeet. Lisätietoja on linkissä [.NET Framework Regular Expressions](http://go.microsoft.com/fwlink/?LinkId=391260). Voit määrittää päivämäärän esitystapoja muokkaamalla Dates.ini-tiedostoa, joka sijaitsee varaston mobiililaiteportaalin palvelimen polussa Content\\Settings\\Dates.ini. Tämä tiedosto käyttää säännönmukaisia .NET-lausekkeita päivämäärämuodon määrittämiseen. Säännönmukaisen lausekkeen tulee sisältää alilausekkeita, jotka luovat nimetyt ryhmät päivälle, kuukaudelle ja vuodelle (PPKKYY) seuraavan esimerkin mukaisesti:

^(?&lt;day&gt;\\d{2})(?&lt;month&gt;\\d{2})(?&lt;year&gt;\\d{2})$

Jokaiseen alilausekkeeseen on kirjoitettava 1-2 numeroa päivän ja kuukauden kohdalle ja 1-4 numeroa vuoden kohdalle. Seuraavassa on alilauseke-esimerkki, joka määrittää nimetyn ryhmän vuodelle ja vaatii vähintään kaksi tai enintään neljä numeroa:

(?&lt;year&gt;\\d{2,4})

Voit määrittää useampia kuin yhden lausekkeen samassa tiedostossa. Jokaisen lausekkeen on oltava erillisenä rivinä. Ensimmäistä täsmäytettyä lauseketta käytetään päivämäärän jäsentämiseen.

<a name="see-also"></a>Lisätietoja
--------

[Varastotyön mobiililaitteiden konfigurointi](configure-mobile-devices-warehouse.md)





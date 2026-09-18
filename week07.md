
## Task 2 – View Wi-Fi Details

I explored the Wi-Fi details of my Windows laptop using the Wi-Fi interface information. The device was connected to the **eduroam** wireless network.

| Parameter | Information |
|---|---|
| **SSID** | eduroam |
| **BSSID** | f4:bd:9e:9e:60:2f |
| **Frequency Band** | 5 GHz |
| **Channel** | 64 |
| **Receive Rate** | 217 Mbps |
| **Transmit Rate** | 287 Mbps |
| **Signal Strength** | 88% |
| **RSSI** | -51 dBm |
| **Network Type** | Infrastructure |
| **Radio Type** | 802.11ax |
| **Authentication** | WPA2-Enterprise |
| **Cipher** | CCMP |
| **Connection Mode** | Auto Connect |

### Discussion

The Wi-Fi connection was using the **eduroam** SSID and was operating on the **5 GHz frequency band on channel 64**. The wireless interface reported a receive rate of **217 Mbps** and a transmit rate of **287 Mbps**. The signal strength was **88%**, with an RSSI of **-51 dBm**.

The connection used **802.11ax** as the radio type. The authentication method was **WPA2-Enterprise**, with **CCMP** as the cipher. The network type was **Infrastructure**, meaning the laptop was connected through a wireless access point.

### Screenshot Evidence

**Figure 1: Wi-Fi details of the eduroam Access Point**
![Github](./images/week7-task2-wifi-details.png)


The screenshot shows the SSID, BSSID, frequency band, channel, data rates, signal strength, authentication method and other connection information collected from the Windows laptop.

# Task 3 – Use Wi-Fi Access Point

I accessed the web management interface of a TP-Link wireless router emulator and explored the available wireless configuration settings. I examined the wireless settings for the 2.4 GHz network and the WPS configuration.

## Current Access Point Settings

The following settings were observed in the TP-Link wireless access point emulator:

| Setting | Current Configuration |
|---|---|
| **Network Name (SSID)** | TP-Link_593D |
| **Wireless Radio** | Enabled |
| **Security** | No Security |
| **Wireless Mode** | 802.11b/g/n mixed |
| **Channel Width** | Auto |
| **Channel** | Auto |
| **Transmit Power** | High |
| **Smart Connect** | Disabled |
| **WPS** | Enabled |
| **WPS Connection Method** | Push Button (Recommended) |
| **Router PIN** | Enabled |

## Important Settings and Recommended Changes

| Setting | Current Setting | Setting I Would Use | Reason |
|---|---|---|---|
| **SSID** | TP-Link_593D | Use a unique and meaningful SSID | A customised SSID makes the network easier to identify and avoids relying on the default network name. |
| **Wireless Security** | No Security | WPA3-Personal, or WPA2/WPA3 if WPA3 is unavailable | The current configuration does not provide wireless authentication or encryption. Using a modern security protocol helps protect wireless communications from unauthorised access. |
| **Wi-Fi Password** | Not configured because security is disabled | Use a long and unique password | A strong password helps prevent unauthorised users from connecting to the network. |
| **Wireless Mode** | 802.11b/g/n mixed | Use a modern Wi-Fi mode supported by the devices | Older wireless standards can reduce network efficiency. Using a suitable modern mode can improve performance when older devices are not required. |
| **Channel Width** | Auto | Use an appropriate channel width based on the wireless environment | Selecting an appropriate channel width can help balance performance and interference. |
| **Channel** | Auto | Select a suitable low-interference channel when necessary | A less congested channel can reduce interference from nearby wireless networks. |
| **Transmit Power** | High | Use an appropriate power level for the required coverage | High transmit power provides greater coverage but can also increase interference with nearby wireless networks. |
| **WPS** | Enabled | Disable WPS if it is not required | Disabling unnecessary WPS functionality reduces the number of wireless access features that could be targeted. |
| **Router PIN** | Enabled | Disable the router PIN if WPS is not required | Disabling unnecessary PIN-based WPS functionality provides an additional security measure. |
| **Smart Connect** | Disabled | Enable only if suitable for the network | Smart Connect can allow compatible devices to be automatically directed between available frequency bands. |

## Discussion of Important Settings

### 1. Wireless Security

The current wireless security setting is **No Security**. I would change this to **WPA3-Personal** if the router and client devices support it. If WPA3 is not available, I would use WPA2/WPA3 or another secure configuration supported by the router.

Using no security means that the wireless network does not require proper authentication or encryption. This could allow unauthorised users to connect to the network and potentially access network resources.

### 2. SSID

The current SSID is **TP-Link_593D**, which appears to be a default-style network name. I would change it to a unique and recognisable name.

A customised SSID makes it easier for users to identify the correct wireless network and avoids confusion with other nearby networks.

### 3. Wireless Password

Because the current security setting is **No Security**, there is no wireless password protecting the network. I would configure a strong and unique Wi-Fi password after enabling WPA3-Personal or another secure authentication method.

The password should be sufficiently long and should not contain easily guessed personal information.

### 4. Wireless Mode

The current wireless mode is **802.11b/g/n mixed**. This configuration supports several generations of Wi-Fi devices, including older standards.

If older devices are not required, I would consider using a more modern wireless mode supported by the access point and client devices. This can improve network efficiency and reduce the need to support outdated wireless standards.

### 5. Channel and Channel Width

The current **channel** and **channel width** are both set to **Auto**. Automatic selection can be useful because the access point can select settings based on the wireless environment.

However, in a congested wireless environment, I would check nearby networks and select a suitable channel with less interference if necessary. I would also select an appropriate channel width based on the amount of interference and performance requirements.

### 6. Transmit Power

The current transmit power is set to **High**. I would choose the transmit power according to the size and requirements of the network.

High power can provide greater coverage, but using unnecessarily high power can increase interference with nearby wireless networks. Therefore, the power level should provide sufficient coverage without unnecessarily increasing interference.

### 7. WPS

The WPS configuration shows that **WPS is enabled**, with the **Push Button** method selected. The router PIN is also enabled.

I would disable WPS if it is not required. WPS provides convenience when connecting devices, but it is not necessary for normal Wi-Fi operation when users can connect using the SSID and secure password.

### 8. Smart Connect

Smart Connect is currently **disabled**. When enabled, the 2.4 GHz and 5 GHz networks can share the same network name and password, allowing compatible devices to automatically switch between bands.

I would consider enabling Smart Connect if the network contains compatible devices and automatic band selection is desirable. Otherwise, keeping it disabled allows the administrator to manage the two frequency bands separately.

## Screenshot Evidence

### Figure 2 – TP-Link Wireless Settings

![Github](./images/week7-task3-TP-Link-Wireless-Settings.png)

The screenshot shows the 2.4 GHz wireless configuration, including the SSID, wireless security, wireless mode, channel width, channel and transmit power settings.

### Figure 3 – TP-Link WPS Settings

![Github](./images/week7-task3-TP-Link-WPS-Settings.png)

The screenshot shows that WPS is enabled and provides the Push Button and PIN connection methods.

## Conclusion

The activity demonstrated that several access point settings affect the security, performance and reliability of a wireless network. The most important settings I would review are wireless security, password configuration, SSID, wireless mode, channel, channel width, transmit power and WPS.

The most significant change I would make to the current configuration is to replace **No Security** with a secure wireless authentication method and use a strong password. I would also disable unnecessary WPS functionality and adjust the channel, channel width and transmit power according to the wireless environment and coverage requirements.

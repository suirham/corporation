# Définir le chemin complet de l'image à utiliser comme fond d'écran
$imagePath = "~\Desktop\image.jpg"

# Utiliser SystemParametersInfo pour changer le fond d'écran
Add-Type -TypeDefinition @"
    using System;
    using System.Runtime.InteropServices;
    public class Wallpaper {
        [DllImport("user32.dll", CharSet = CharSet.Auto)]
        public static extern int SystemParametersInfo(int uAction, int uParam, string lpvParam, int fuWinIni);
    }
"@
[Wallpaper]::SystemParametersInfo(20, 0, $imagePath, 3)

<?php
function decryptCaesar($text, $shift) {
    $result = '';
    $characters = str_split($text);
    foreach ($characters as $character) {
        if (ctype_upper($character)) {
            $ascii = ord('A');
        } else if (ctype_lower($character)) {
            $ascii = ord('a');
        } else {
            $result .= $character;
            continue;
        }
        $decryptedCharCode = ((ord($character) - $ascii - $shift) % 26) + $ascii;
        $result .= chr($decryptedCharCode);
    }
    return $result;
}

function tryVariousShifts($text) {
    for ($shift = 0; $shift < 26; $shift++) {
        echo "Shift: $shift - ";
        echo decryptCaesar($text, $shift) . "\n";
    }
}

tryVariousShifts("UW GURUVW JRA VGYZ! DG TB KS TBRZXYWW! WN JREJL DG VQ HFR WR WYW.");
?>

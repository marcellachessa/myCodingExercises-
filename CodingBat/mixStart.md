Return true if the given string begins with "mix", except the 'm' can be anything, so "pix", "9ix" .. all count.

mixStart("mix snacks") → true
mixStart("pix snacks") → true
mixStart("piz snacks") → false

(```)
public boolean mixStart(String str) {
if (str.startsWith("mix",0)) {
return true;
}
if (str.startsWith("pix",0)) {
return true;
}
if (str.startsWith("nix",0)) {
return true;
}
return false;
}
(```)

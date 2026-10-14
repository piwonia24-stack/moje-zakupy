MOJE ZAKUPY — aplikacja PWA

CO DZIAŁA
- Dodawanie zakupów, 10 kategorii, ilości i jednostki.
- Sortowanie A–Z / Z–A, filtrowanie, odhaczanie.
- Kupione pozycje przesuwają się na dół.
- Baza produktów zachowuje produkty po wyczyszczeniu listy.
- Lokalny zapis na urządzeniu, eksport/import kopii.
- Opcjonalna synchronizacja w czasie rzeczywistym przez Firebase Firestore.

WAŻNE
Pliki stanowią gotową aplikację webową, ale nie są jeszcze opublikowane pod publicznym adresem. Żeby dodać ikonę na iPhonie, najpierw trzeba opublikować pliki pod adresem HTTPS (np. Firebase Hosting). Synchronizacja między dwoma telefonami wymaga skonfigurowania Firebase.

KONFIGURACJA SYNCHRONIZACJI
1. Utwórz projekt w Firebase Console: https://console.firebase.google.com/
2. Dodaj aplikację Web i skopiuj apiKey, authDomain, projectId, appId oraz messagingSenderId.
3. Włącz Firestore Database.
4. Wdróż aplikację pod HTTPS. Otwórz ją na obu telefonach.
5. W Ustawieniach wpisz dane Firebase oraz ten sam trudny do odgadnięcia kod listy na obu urządzeniach.

BEZPIECZEŃSTWO
Ten prototyp zapisuje dokument pod ścieżką shoppingLists/{kod}. Sam kod nie stanowi silnego uwierzytelniania. Przed użyciem do prywatnych danych skonfiguruj reguły Firestore i uwierzytelnianie użytkowników; nie pozostawiaj bazy otwartej publicznie. Do użytku rodzinnego zalecane jest dodanie Firebase Authentication i reguł dostępu ograniczonych do członków listy.

PUBLIKACJA
Można użyć Firebase Hosting. W katalogu umieść index.html, manifest.json i sw.js, a następnie wdroż przez Firebase CLI.

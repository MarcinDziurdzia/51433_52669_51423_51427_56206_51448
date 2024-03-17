2. **Skonfiguruj strukturę projektu oraz ustawienia**:
   - W folderze "library_backend" znajdziesz następujące pliki i foldery:
     - **manage.py**: Narzędzie wiersza poleceń do zarządzania projektem.
     - **library_backend/**: Główny pakiet projektu.
       - **settings.py**: Ustawienia projektu (baza danych, middleware, aplikacje, itp.).
       - **urls.py**: Konfiguracja adresów URL dla projektu.
       - **asgi.py**: Konfiguracja ASGI (dla obsługi asynchronicznej).
       - **wsgi.py**: Konfiguracja WSGI (do wdrożenia).
     - **db.sqlite3**: Domyślna baza danych SQLite (możesz to zmienić w ustawieniach).

   - W pliku **settings.py** możesz dostosować:
     - Ustawienia bazy danych (np. PostgreSQL, MySQL).
     - Dodane aplikacje (np. 'django.contrib.admin', 'django.contrib.auth', 'django.contrib.contenttypes', itp.).
     - Strefę czasową (TIME_ZONE), adres URL dla plików statycznych (STATIC_URL) i inne ustawienia specyficzne dla projektu.

3. **Utwórz nową aplikację o nazwie "library"**:
   - W terminalu wykonaj polecenie:
     ```
     python manage.py startapp library
     ```
   - W folderze "library" znajdziesz pliki takie jak:
     - **admin.py**: Rejestracja modeli w panelu administracyjnym Django.
     - **apps.py**: Konfiguracja aplikacji.
     - **models.py**: Definicje modeli bazy danych (np. Book, Author, itp.).
     - **views.py**: Widoki (endpointy API).
     - **serializers.py**: Serializatory dla modeli (używając Django REST framework).
     - **tests.py**: Testy dla Twojej aplikacji.
     - **urls.py**: Definicje adresów URL dla aplikacji.

   - W aplikacji "library" możesz:
     - Zdefiniować modele (np. Book, Author) w pliku **models.py**.
     - Tworzyć widoki (używając funkcji lub klas) w pliku **views.py**.
     - Skonfigurować adresy URL w pliku **urls.py**.

4. **Uruchom migracje, aby utworzyć tabele w bazie danych**:
   ```
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Utwórz superusera (administratora) dla panelu administracyjnego**:
   ```
   python manage.py createsuperuser
   ```

6. **Uruchom serwer deweloperski**:
   ```
   python manage.py runserver
   ```
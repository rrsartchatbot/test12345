---
description: >-
  Jako technologia na wczesnym etapie, Duet AI może generować dane wyjściowe
  wydaje się to prawdopodobne, ale jest błędne. Zalecamy sprawdzenie wszystkich
  danych wyjściowych z Duet AI zanim go użyjesz.
---

# Koduj z pomocą Duet AI

## Koduj z pomocą Duet AI





* Podaj wskazówki, które pomogą Ci rozwiązać problemy z kodem.
* Wygeneruj kod dla swojego projektu.
* Otrzymuj wbudowane sugestie podczas kodowania.

Duet AI nie wykorzystuje Twoich podpowiedzi ani odpowiedzi jako danych do uczenia swojego modelu. Dla więcej informacji zob [Jak Duet AI w Google Cloud wykorzystuje Twoje dane](https://cloud.google.com/duet-ai/docs/discover/data-governance).

Aby pomóc Ci spełnić wymagania z wszelkimi wymaganiami licencyjnymi dotyczącymi Twojego kodu, jakie zapewnia Duet AI cytaty źródłowe, gdy sugestie bezpośrednio cytują konkretny fragment źródło. Aby dowiedzieć się więcej o tym, jak i kiedy Duet AI cytuje źródła, zobacz [Jak Duet AI pomaga w generowaniu kodu i cytuje źródła](https://cloud.google.com/duet-ai/docs/discover/code-generation-source-citation#how-when-duet-ai-cites-sources).

Ten dokument jest przeznaczony dla programistów na wszystkich poziomach umiejętności. Zakłada, że ​​ty posiadać praktyczną wiedzę na temat VS Code i znasz Google Cloud. Jeśli wolisz, możesz także poznać Duet AI w [Stacje robocze w chmurze](https://cloud.google.com/workstations/docs/write-code-duet-ai), [Kod Cloud dla IntelliJ](https://cloud.google.com/code/docs/intellij/write-code-duet-ai) oraz [Edytor Cloud Shell](https://cloud.google.com/code/docs/shell/write-code-duet-ai).

### Zanim zaczniesz <a href="#before_you_begin" id="before_you_begin"></a>

1.  W konsoli Google Cloud na stronie wyboru projektu wybierz lub [utwórz projekt Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

    Uwaga: jeśli nie planujesz zachować zasoby utworzone w ramach tej procedury zamiast tego utwórz projekt wybór istniejącego projektu. Po wykonaniu tych kroków będzie to możliwe usuń projekt, usuwając wszystkie zasoby powiązane z projektem.

    [Przejdź do selektora projektów](https://console.cloud.google.com/projectselector2/home/dashboard)
2. [Upewnij się, że w Twoim projekcie Google Cloud włączone są płatności](https://cloud.google.com/billing/docs/how-to/verify-billing-enabled#console).
3. [Upewnij się, że Duet AI jest skonfigurowany swoje konto użytkownika i projekt Google Cloud.](https://cloud.google.com/duet-ai/docs/discover/set-up-duet-ai)
4. Zainstaluj [rozszerzenie Cloud Code](https://cloud.google.com/code/docs/vscode/install#install) jeśli jeszcze tego nie zrobiłeś. Cloud Code integruje się z Duet AI w Twoim IDE.
5. Opcjonalnie: jeśli zdecydujesz się sklonować próbkę zadań z tego dokumentu, zainstaluj [Gita](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). Do kopiowania próbek na Twoją maszynę wymagany jest Git.

### Włącz Duet AI w Cloud Code <a href="#enable-duet-ai-in-cloud-code" id="enable-duet-ai-in-cloud-code"></a>

W tej sekcji możesz połączyć się z Google Cloud i włączyć tę funkcję Duet AI w jedziesz.

Jeśli wolisz postępować zgodnie z instrukcją **Koduj za pomocą Duet AI** bezpośrednio w swoim IDE, kliknij **Uruchom kod VS** i postępuj zgodnie z instrukcjami w instrukcja łączenia się z Google Cloud i aktywacji Duet AI.

[Uruchom kod VS](vscode://googlecloudtools.cloudcode/cloudcode.openWalkthrough?id=duet-ai)

W przeciwnym razie wykonaj następujące kroki:

1. Uruchom swój IDE.
2.  W na pasku stanu kliknij **Cloud Code – Zaloguj się**.

    ![Cloud Code — przycisk Zaloguj się na pasku stanu.](https://cloud.google.com/static/code/docs/vscode/images/cloud-code-sign-in-status-bar.png)
3. Po wyświetleniu monitu o zezwolenie Cloud Code na otwarcie zewnętrznej witryny internetowej kliknij **Otwórz**.
4. Postępuj zgodnie z instrukcjami, aby zalogować się na swoje konto Google.
5.  Po wyświetleniu monitu o upewnienie się, że pobrałeś Cloud Code od Google, kliknij **Zaloguj się**.

    Masz teraz połączenie z Google Cloud.

Następnie musisz włączyć Duet AI w Cloud Code. Zanim kontynuując te kroki, postępuj zgodnie z instrukcjami w [Skonfiguruj Duet AI dla projektu](https://cloud.google.com/duet-ai/docs/discover/set-up-duet-ai), jeśli jeszcze tego nie zrobiłeś.

Aby włączyć Duet AI w Cloud Code dla jedziesz, podążaj za nimi kroki:

1. W Twoim IDE wybierać **Kod** (dla MacOS) lub **Plik** (dla Windows i Linux), a następnie przejdź do **Ustawienia** > **Ustawienia**.
2. Na karcie **Użytkownik** w oknie dialogowym **Ustawienia** kliknij przejdź do **Rozszerzenia** > **Google Cloud Code**.
3. Przewiń, aż znajdziesz **Duet AI: Włącz**, a następnie wybierz opcję **Włącz Duet Pole wyboru AI dla programistów**.
4.  Załaduj ponownie swoje IDE.

    Dzięki temu możliwe jest włączenie Duet AI w Cloud Code oraz **Duet AI** pojawia się pasek stanu jedziesz.

    ![Pasek stanu Duet AI jest dostępny.](https://cloud.google.com/static/code/docs/vscode/images/duet-ai-status-bar-no-project-selected.png)
5.  Wybierz projekt Google Cloud, który ma interfejs API Cloud AI Companion włączony:

    1. Na pasku stanu **Duet AI** kliknij **Duet AI**.
    2. W menu **Szybki wybór Duet AI** wybierz projekt Google Cloud z włączonym interfejsem API Cloud AI Companion.

    Duet AI jest gotowy do użycia.

    ![Ikona Duet AI na pasku stanu jest ustawiona na normalną.](https://cloud.google.com/static/code/docs/vscode/images/duet-ai-status-bar-project-selected.png)

    Jeśli wybierzesz projekt Google Cloud bez Włączono interfejs Cloud AI Companion API, otrzymasz powiadomienie o błędzie i zostali poinstruowani, aby skontaktować się z administratorem. Aby uzyskać więcej informacji, zobacz [Skonfiguruj Duet AI dla projektu](https://cloud.google.com/duet-ai/docs/discover/set-up-duet-ai).

Aby przetestować możliwości Duet AI, otwórz aplikację lub utwórz przykładową aplikację w następnej sekcji.

### Opcjonalnie: Utwórz przykładową aplikację <a href="#optional_create_a_sample_application" id="optional_create_a_sample_application"></a>

Jeśli wolisz skorzystać z istniejącej aplikacji, aby przetestować możliwości Duet AI, możesz pominąć tę sekcję. W przeciwnym razie, aby utworzyć plik przykładową aplikację, wykonaj następujące kroki:

1. W swoim IDE otwórz paletę poleceń: albo naciśnij Control+Shift+P (w systemach Windows i Linux) lub Command+Shift+P (dla MacOS), a następnie uruchom **Cloud Code: New Zastosowanie**.
2. Wybierz **aplikację Kubernetes**.
3. Wybierz szablon aplikacji **Python (Flask): Księga gości**.
4.  Zapisz nowe aplikację w preferowanej lokalizacji.

    Powiadomienie potwierdza utworzenie aplikacji i otwiera nowe okno otwiera się z załadowaną aplikacją.

### Czatuj z Duet AI <a href="#chat-with-duet-ai" id="chat-with-duet-ai"></a>

W tej sekcji dowiesz się, jak otworzyć panel **Duet AI** i porozmawiać z Duet AI, aby uzyskać wyjaśnienie istniejącego kodu.

Aby rozpocząć rozmowę z Duet AI, wykonaj następujące kroki:

1. Utwórz nowy lub użyj istniejącego pliku kodu. Jeśli używasz języka Python (Flask) przykład, możesz wykonać to zadanie w swoim pliku `front.py`: przejdź do **Eksplorator** > **src** > **frontend** i otwórz plik `front.py` plik.
2. Na pasku aktywności twojego IDE, Kliknijchat\_spark **Duet AI**.
3.  W panelu **Duet AI** wpisz zachętę `Explain this code to me` i kliknij wysłać **Wyślij**.

    Duet AI używa kodu z pliku kodu jako odniesienia do monit i odpowie objaśnieniem kodu.

    Aby odnieść się do konkretnego bloku kodu zamiast do całego kodu w pliku, ty możesz wybrać blok w pliku kodu, a następnie wyświetlić monit Duet AI.

#### Zresetuj historię czatów <a href="#reset_chat_history" id="reset_chat_history"></a>

Duet AI wykorzystuje historię czatów dla dodatkowego kontekstu, kiedy odpowiadając na Twoje podpowiedzi.

Jeśli Twoja historia czatów nie jest już istotna dla tego, co próbujesz osiągnąć, możesz to zrobić możesz zresetować historię czatów: w panelu **Duet AI** kliknij usuwać **Zresetuj czat**.

**Uwaga:** Historia czatów resetuje się automatycznie po zmianie obszaru roboczego lub zamknij swoje IDE.

### Wygeneruj kod z podpowiedziami <a href="#generate_code_with_prompts" id="generate_code_with_prompts"></a>

W poniższych sekcjach pokazano, jak używać Duet AI do generowania kod z przykładowym monitem `# Function to create a Cloud Storage bucket` wewnątrz pliku Pythona. Możesz także wybrać część kodu, a następnie poproś Duet AI o pomoc poprzez funkcję czatu oraz odbieraj i akceptuj lub odrzucaj sugestie dotyczące kodów kodujesz.

#### Zapytaj Duet AI w pliku kodu <a href="#prompt-duet-ai-in-code-file" id="prompt-duet-ai-in-code-file"></a>

1. Utwórz nowy lub użyj istniejącego pliku kodu. Jeśli używasz języka Python (Flask) próbkę, możesz to zrobić w swoim pliku `front.py`: przejdź do **Eksploratora** > **src** > **frontend** i otwórz plik `front.py`.
2. W pliku kodu w nowej linii wpisz `# Function to create a Cloud Storage bucket`, a następnie naciśnij Enter (dla Windows i Linux) lub Return (dla systemu MacOS).
3.  Aby wygenerować kod, naciśnij Control+Enter (dla Windows i Linux) lub Control+Return (dla systemu MacOS).

    Obok tekstu zachęty w pliku Pythona Duet AI generuje kod w postaci tekstu-ducha.
4. Opcjonalnie: Aby zaakceptować wygenerowany kod, naciśnij Tab.

#### Zapytaj Duet AI o wybrany kod za pomocą czatu <a href="#prompt-duet-ai-chat" id="prompt-duet-ai-chat"></a>

Duet AI może wykonywać zadania lub odpowiadać na Twoje pytania w oparciu o wybrany przez Ciebie kod. Aby uzyskać wygenerowany kod oparty na podpowiedzi za pomocą wybrany kod, wykonaj następujące kroki:

1. W jedziesz, otwórz plik w swoim projekcie zawierający kod lub użyj tego samego pliku kodu, który użyłeś w poprzednich krokach.
2. Na pasku aktywności kliknijchat\_spark **Duet AI**, aby otworzyć panel **Duet AI**.
3. W pliku kodu wybierz blok kodu.
4.  W polu tekstowym panelu **Duet AI** wpisz monit o podanie wybranego kodu.

    Na przykład wybierz funkcję w swoim kodzie i wprowadź zachętę `Write a unit test for this function`:

    ![Duet AI pisze test jednostkowy dla wybranej funkcji.](https://cloud.google.com/static/code/docs/vscode/images/duet-ai-unit-test-prompt-example.png)

    Duet AI używa wybranego kodu jako odniesienia i odpowiada na Twój monit.

#### Otrzymuj sugestie wbudowane podczas kodowania <a href="#get_inline_suggestions_while_you_code" id="get_inline_suggestions_while_you_code"></a>

Podczas pisania kodu Duet AI wyświetla sugestie dotyczące kodu wbudowanego które możesz zaakceptować lub zignorować. Aby wypróbować tę funkcję, wykonaj następujące kroki:

1. Utwórz nowy lub użyj istniejącego pliku kodu. Jeśli używasz języka Python (Flask) próbkę, możesz to zrobić w swoim pliku `front.py`: przejdź do **Eksploratora** > **src** > **frontend** i otwórz plik `front.py`.
2.  W pliku kodu, w nowej linii rozpocznij pisanie funkcji. Na przykład, jeśli jesteś w pliku Pythona, napisz `def`.

    Duet AI sugeruje kod w postaci tekstu-ducha.
3. Aby zaakceptować sugestię kodu od Duet AI, naciśnij Tab. W przeciwnym razie, aby zignorować sugestię, naciśnij Esc lub kontynuuj pisanie kodu.

**Opcjonalnie: wyłącz sugestie wbudowane**

Jeśli wolisz wyłączyć sugestie wbudowane w Duet AI, wykonaj poniższe czynności te kroki:

1. W Twoim IDE wybierać **Kod** (dla MacOS) lub **Plik** (dla Windows i Linux), a następnie przejdź do **Ustawienia** > **Ustawienia**.
2. Na karcie **Użytkownik** w oknie dialogowym **Ustawienia** kliknij przejdź do **Rozszerzenia** > **Kod Cloud**.
3.  Przewiń, aż znajdziesz **Cloudcode: Duet AI: Inline Sugestie: Włącz Lista automatyczna**, a następnie wybierz **Wyłączone**.

    To wyłącza sugestie wbudowane. Nadal możesz nacisnąć Control+Enter (dla systemów Windows i Linux) lub Control+Return (dla systemu MacOS), aby ręcznie uruchamiać wbudowane sugestie.

### Używaj mądrych działań <a href="#use_smart_actions" id="use_smart_actions"></a>

Aby pomóc Ci zwiększyć produktywność przy jednoczesnej minimalizacji przełączania kontekstu, Duet AI zapewnia _inteligentne działania_ oparte na sztucznej inteligencji bezpośrednio w Twoim edytor kodu. Po wybraniu kodu w edytorze kodu możesz wyświetlić i wybierz z listy działań odpowiednich do Twojego kontekstu.

Aby użyć inteligentnych akcji w swoim kodzie, wykonaj następujące kroki:

1. W pliku kodu wybierz blok kodu.
2. Kliknij obok wybranego bloku kodu żarówka **Więcej działań**.
3.  Wybierz akcję, np. **Generuj testy jednostkowe**.

    Duet AI generuje odpowiedź na podstawie wykonanej przez Ciebie akcji wybrany.

### Przetestuj inne przykładowe monity <a href="#test_other_example_prompts" id="test_other_example_prompts"></a>

Po przeczytaniu [Generuj kod z podpowiedziami](https://cloud.google.com/code/docs/vscode/write-code-duet-ai#generate\_code\_with\_prompts) w tej sekcji dokumentu, wypróbuj niektóre z poniższych przykładowych podpowiedzi.

#### Uzyskaj wyjaśnienie kodu <a href="#get_an_explanation_of_code" id="get_an_explanation_of_code"></a>

1. W pliku kodu wybierz funkcję, którą chcesz wyjaśnić.
2.  W panelu **Duet AI** wpisz zachętę `Explain this code to me`.

    Duet AI używa wybranego kodu jako odniesienia i odpowiada objaśnieniem wybranej funkcji.

#### Generuj plany testów <a href="#generate_test_plans" id="generate_test_plans"></a>

1. W pliku kodu wybierz kod, dla którego chcesz dodać testy jednostkowe.
2. W panelu **Duet AI** wpisz zachętę `Write unit tests for my code`.

#### Uzyskaj pomoc dotyczącą debugowania kodu <a href="#get_help_with_debugging_code" id="get_help_with_debugging_code"></a>

1. W pliku kodu wybierz kod, który chcesz debugować.
2. W panelu **Duet AI** wpisz zachętę `Help me debug my code`.

#### Spraw, aby Twój kod był bardziej czytelny <a href="#make_your_code_more_readable" id="make_your_code_more_readable"></a>

1. W pliku kodu wybierz kod, który chcesz zwiększyć czytelność.
2.  W panelu **Duet AI** wpisz zachętę `Make my code more readable`.

    Jeśli wolisz skupić się na określonej części kodu, wybierz opcję preferowaną część kodu przed zapytaniem Duet AI.

### Znane problemy <a href="#known_issues" id="known_issues"></a>

W poniższych sekcjach omówiono znane problemy związane z Duet AI w Cloud Code.

#### Odpowiedzi na czacie mogą zostać obcięte, jeśli zawierają zaktualizowaną wersję dużego, otwartego pliku <a href="#chat_responses_may_be_truncated_when_they_include_an_updated_version_of_a_large_open_file" id="chat_responses_may_be_truncated_when_they_include_an_updated_version_of_a_large_open_file"></a>

Aby obejść ten problem, wybierz mniejszą sekcję kodu i dołącz plik dodatkowa dyrektywa w wierszu poleceń, np`only output the selected code.`

#### Vim: Nie można zaakceptować ani odrzucić sugestii dotyczących generowania kodu, chyba że jest w trybie wstawiania <a href="#vim_cannot_accept_or_dismiss_code_generation_suggestions_unless_in_insert_mode" id="vim_cannot_accept_or_dismiss_code_generation_suggestions_unless_in_insert_mode"></a>

Używając wtyczki Vima w trybie normalnym, nie możesz zaakceptować ani odrzucić kodu propozycje.

Aby obejść ten problem, naciśnij i, aby przejść do trybu wstawiania, a następnie naciśnij Tab, aby zaakceptować sugestię.

#### Vim: Niespójne zachowanie po naciśnięciu Esc w celu odrzucenia sugestii <a href="#vim_inconsistent_behavior_when_pressing_esc_to_dismiss_suggestions" id="vim_inconsistent_behavior_when_pressing_esc_to_dismiss_suggestions"></a>

Po naciśnięciu Esc zarówno IntelliJ, jak i Duet AI sugestie są odrzucane. To zachowanie różni się od zachowania innego niż Vim gdzie naciśnięcie Esc powoduje ponowne uruchomienie Duet AI.

#### Ostrzeżenia o podaniu licencji nie są wyświetlane w trakcie sesji <a href="#license_recitation_warnings_dont_persist_across_sessions" id="license_recitation_warnings_dont_persist_across_sessions"></a>

Jeśli ostrzeżenia dotyczące informacji o licencji nie wyświetlają się w trakcie sesji, zapoznaj się z sekcją trwałe logi:

1. Kliknij **Widok** > **Wyjście**.
2. Wybierz **Duet AI – Cytaty**.

#### Problemy z łącznością w oknie wyjściowym Duet AI <a href="#connectivity-issues" id="connectivity-issues"></a>

Jeśli widzisz błąd połączenia lub inne problemy z łącznością w pliku W oknie wyjściowym Duet AI spróbuj wykonać następujące czynności:

* Skonfiguruj zaporę sieciową, aby umożliwić dostęp do `oauth2.googleapis.com` i `cloudaicompanion.googleapis.com`.
* Skonfiguruj zaporę tak, aby zezwalała na komunikację za pośrednictwem protokołu HTTP/2, z którego korzysta gRPC.

Możesz użyć narzędzia `grpc-health-probe` do przetestowania łączności. Sukces sprawdź wyniki w następującym wyniku:

`$ grpc-health-probe -addr cloudaicompanion.googleapis.com:443 -tls error: this server does not implement the grpc health protocol (grpc.health.v1.Health): GRPC target method can't be resolved`

Nieudana kontrola skutkuje następującym wynikiem:

`timeout: failed to connect service "cloudaicompanion.googleapis.com:443" within 1s`

Aby uzyskać więcej szczegółów, wykonaj następujące polecenie przed `grpc-health-probe`:

```
export GRPC_GO_LOG_SEVERITY_LEVEL=info
```

### Wystawić opinię <a href="#leave_feedback" id="leave_feedback"></a>

Aby zostawić opinię na temat swoich doświadczeń, wykonaj następujące kroki:

1. Na pasku stanu kliknij **Duet AI**, a następnie w **Szybki wybór** menu, wybierz **Prześlij opinię**.
2. W formularzu wypełnij **Tytuł** i Pola **Komentarze**.
3. Jeśli chcesz udostępnić swoje logi Skaffold lub AI Companion, upewnij się, że wybrałeś **Wyślij logi Skaffold** lub **Wyślij logi AI Companion**.
4. Kliknij **Prześlij opinię**.

### Co dalej <a href="#whats_next" id="whats_next"></a>

* Dowiedz się, jak [pisać lepsze podpowiedzi](https://cloud.google.com/duet-ai/docs/discover/write-prompts).

Makarenko Alyona

e-mail: alyonka.m.by@gmail.com
telegram: str_ind

A person who works well under the pressure and exudes positivity and confidence - that's all about me. I always look for ways to self-improvement, that's the reason I'm here)

Skills: C++, QT, C#, Python, Unity

Code example: 
    std::string tmp = ui->text_get->toPlainText().toStdString();
    std::regex regular("(class|struct)\\s+(\\w|\\d|_)+\\s*\\{");
    std::smatch res;

    size_t class_c = 0;
    size_t struct_c = 0;

    while (std::regex_search(tmp, res, regular)) {
        std::string example;
        int i = 6;
        int whatisit = 0;
        if (res.str()[i] == ' ') {++i; ++whatisit;}
        while (res.str()[i] != ' ' && res.str()[i] != '{')
            example += res.str()[i++];
        tmp = res.suffix();

        size_t indexclose = tmp.find_first_of("}");
        if (indexclose == std::string::npos) { QMessageBox::warning(nullptr, "Error", "you forgot to put '}"); return;}
        size_t indexopen = tmp.find_first_of("{");
        while (indexclose > indexopen) {
            indexclose = tmp.find_first_of("}", indexclose + 1);
            indexopen = tmp.find_first_of("{", indexclose);
            if (indexclose == std::string::npos) { QMessageBox::warning(nullptr, "Error", "you forgot to put '}"); return;}
        }

Education: student of Belarussian State University of Informatics and Radioelectronics (BSUIR), major in informatics and technologies of programming (faculty of computer systems and networks).

Level of English: C1 (finished Streamline C1+ courses)

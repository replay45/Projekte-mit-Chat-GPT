import PyPDF2

def pdf_passwort_schutz(input_pdf, output_pdf, passwort):
    # PDF-Datei zum Lesen öffnen
    with open(input_pdf, 'rb') as pdf_file:
        # PDF-Reader-Objekt erstellen
        pdf_reader = PyPDF2.PdfFileReader(pdf_file)

        # PDF-Writer-Objekt erstellen
        pdf_writer = PyPDF2.PdfFileWriter()

        # Durch jede Seite des Original-PDFs iterieren
        for page_num in range(pdf_reader.numPages):
            # Seite hinzufügen
            pdf_writer.addPage(pdf_reader.getPage(page_num))

        # Passwort zum PDF hinzufügen
        pdf_writer.encrypt(passwort)

        # Ausgabedatei zum Schreiben öffnen
        with open(output_pdf, 'wb') as output_file:
            # Geschütztes PDF schreiben
            pdf_writer.write(output_file)

if __name__ == "__main__":
    # Beispielaufruf des Programms
    input_pdf_path = 'pfad/zur/deiner/input.pdf'
    output_pdf_path = 'pfad/zur/deiner/output-pw-geschützt.pdf'
    password = 'dein_passwort'

    pdf_passwort_schutz(input_pdf_path, output_pdf_path, password)
    print(f'PDF wurde erfolgreich mit dem Passwort geschützt: {output_pdf_path}')

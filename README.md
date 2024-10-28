# -Criando-um-Ebook-com-ChatGPT-MidJourney
import nl.siegmann.epublib.domain.Book;
import nl.siegmann.epublib.domain.Resource;
import nl.siegmann.epublib.domain.Section;
import nl.siegmann.epublib.epub.EpubWriter;

import java.io.FileOutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.net.URL;

public class EbookCreator {

    public static void main(String[] args) {
        try {
            // Criação do livro
            Book book = new Book();
            book.getMetadata().addTitle("Criando um Ebook com ChatGPT e MidJourney");
            book.getMetadata().addAuthor("Seu Nome");

            // Conteúdo fictício para o livro (gerado via ChatGPT)
            String textoCapitulo1 = "Bem-vindo ao eBook sobre a criação de conteúdo usando ChatGPT e MidJourney.";
            String textoCapitulo2 = "ChatGPT é uma poderosa ferramenta para geração de textos.";
            String textoCapitulo3 = "MidJourney pode gerar imagens incríveis para enriquecer o conteúdo visual do seu livro.";

            // Adicionando capítulos como seções
            book.addSection("Introdução", new Resource(textoCapitulo1.getBytes(), "intro.html"));
            book.addSection("Capítulo 1 - ChatGPT", new Resource(textoCapitulo2.getBytes(), "chatgpt.html"));
            book.addSection("Capítulo 2 - MidJourney", new Resource(textoCapitulo3.getBytes(), "midjourney.html"));

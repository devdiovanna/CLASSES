package br.com.letscode.java;

import java.time.LocalDate;
import java.time.LocalTime;
import java.util.Locale;
import java.time.format.TextStyle;

public class Main {

    public static void main(String[] args) {

        String nome = "Jessé";

        LocalDate hoje = LocalDate.now();
        Locale brasil = new Locale("pt", "BR");
        String diaSemana = hoje.getDayOfWeek().getDisplayName(TextStyle.FULL, brasil);

        LocalTime agora = LocalTime.now();

        String saudacao = "";
        switch (agora.getHour()) {
            case 0:
            case 1:
            case 2:
            case 3:
            case 4:
            case 5:
            case 6:
            case 7:
            case 8:
                saudacao = "bom dia";
                break;
            case 9:
            case 10:
            case 11:
            case 12:
                saudacao = "boa tarde";
                break;
            case 13:
            case 14:
            case 15:
            case 16:
            case 17:
                saudacao = "boa tarde";
                break;
            case 18:
            case 19:
            case 20:
            case 21:
            case 22:
            case 23:
                saudacao = "boa noite";
                break;
            default:
                saudacao = "Hora inválida";
                break;
        }

        System.out.println("Olá, " + nome + ". Hoje é " + diaSemana + ", " + saudacao + ".");
    }
}

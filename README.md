# Object-Oriented-Racing-Game
This project is a intro to Java object-oriented racing game developed in Visual Basic. The game functions similar to Mario Kart while also allowing users to win and bet credits on participants as well as collect and purchase prizes from a virtual shop.
Public Class Form1

    'Variables for setting up the race are introduced. 
    Dim RacerCount As String

    'Variables for betting are introduced.
    Dim Credits = 1000
    Dim WinnerPrediction As String
    Dim Gamble As Integer
    Dim RaceWinner As String

    'Variables for how far each racer moves per 100 milliseconds are introduced.
    Dim iRand1 As Integer
    Dim iRand2 As Integer
    Dim iRand3 As Integer
    Dim iRand4 As Integer
    Dim iRand5 As Integer
    Dim iRand6 As Integer

    'Varibles to track stats are introduced.
    Dim NarutoWins = 0
    Dim KakashiWins = 0
    Dim ObitoWins = 0
    Dim MadaraWins = 0
    Dim ItachiWins = 0
    Dim SasukeWins = 0

    'Variables for prize shop are introduced.
    Dim PrizeChoice As String

   

 

    Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

        'Hide the racers until the user has chosen how many participants he wants to race.
        PictureBox1.Visible = False
        PictureBox2.Visible = False
        PictureBox3.Visible = False
        PictureBox4.Visible = False
        PictureBox5.Visible = False
        PictureBox6.Visible = False


    End Sub

    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click

        'Welcome the user to the game and give them a start balance for betting.
        MsgBox("Welcome to AnimeRacing! You have been given 1000 credits to start off.")
        Label1.Text = "Bank Balance: " & Credits & " Credits"

        'Guide the user to set up the race how they desire it to be.
        MsgBox("Please select the amount of racers you want to race by clicking on one of the blue buttons")

    End Sub

    Private Sub Button2_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button2.Click

        'Make the participating racers visible and keep the rest hidden.
        PictureBox1.Visible = True
        PictureBox2.Visible = True
        PictureBox3.Visible = False
        PictureBox4.Visible = False
        PictureBox5.Visible = False
        PictureBox6.Visible = False

        'Set the amount of racers into the variable.
        RacerCount = 2

        'Let the user guess who will win the race. Check for errors and then let the user know the race is ready to begin.
        WinnerPrediction = InputBox("Before the race begins, who do you think will win? Enter the name of the racer you bet on!")

        If WinnerPrediction = "Naruto" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Kakashi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Obito" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Madara" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Itachi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Sasuke" Then
            MsgBox("May the odds be ever in your favour!")
        Else
            MsgBox("Please enter one of the following: ( Naruto | Kakashi | Obito | Madara | Itachi | Sasuke )")
        End If

        'The user decides how many credits they want to bet on the race.
        Gamble = InputBox("How many credits would you like to bet?")

        If Gamble > Credits Then
            MsgBox("You don't have that many credits. Try betting less credits")
        ElseIf Gamble < Credits Then
            MsgBox("Your bet has been received. The racers are ready. Click on the yellow 'Start Race' button to begin the race.")
        Else
            MsgBox("Make sure to enter a whole number as the numerical value")
        End If

    End Sub

    Private Sub Button3_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button3.Click

        'Make the participating racers visible and keep the rest hidden.
        PictureBox1.Visible = True
        PictureBox2.Visible = True
        PictureBox3.Visible = True
        PictureBox4.Visible = False
        PictureBox5.Visible = False
        PictureBox6.Visible = False

        'Set the amount of racers into the variable.
        RacerCount = 3

        'Let the user guess who will win the race. Check for errors and then let the user know the race is ready to begin.
        WinnerPrediction = InputBox("Before the race begins, who do you think will win? Enter the name of the racer you bet on!")

        If WinnerPrediction = "Naruto" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Kakashi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Obito" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Madara" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Itachi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Sasuke" Then
            MsgBox("May the odds be ever in your favour!")
        Else
            MsgBox("Please enter one of the following: ( Naruto | Kakashi | Obito | Madara | Itachi | Sasuke )")
        End If

        'The user decides how many credits they want to bet on the race.
        Gamble = InputBox("How many credits would you like to bet?")

        If Gamble > Credits Then
            MsgBox("You don't have that many credits. Try betting less credits")
        ElseIf Gamble < Credits Then
            MsgBox("Your bet has been received. The racers are ready. Click on the yellow 'Start Race' button to begin the race.")
        Else
            MsgBox("Make sure to enter a whole number as the numerical value")
        End If

    End Sub

    Private Sub Button4_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button4.Click

        'Make the participating racers visible and keep the rest hidden.
        PictureBox1.Visible = True
        PictureBox2.Visible = True
        PictureBox3.Visible = True
        PictureBox4.Visible = True
        PictureBox5.Visible = False
        PictureBox6.Visible = False

        'Set the amount of racers into the variable.
        RacerCount = 4

        'Let the user guess who will win the race. Check for errors and then let the user know the race is ready to begin.
        WinnerPrediction = InputBox("Before the race begins, who do you think will win? Enter the name of the racer you bet on!")

        If WinnerPrediction = "Naruto" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Kakashi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Obito" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Madara" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Itachi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Sasuke" Then
            MsgBox("May the odds be ever in your favour!")
        Else
            MsgBox("Please enter one of the following: ( Naruto | Kakashi | Obito | Madara | Itachi | Sasuke )")
        End If

        'The user decides how many credits they want to bet on the race.
        Gamble = InputBox("How many credits would you like to bet?")

        If Gamble > Credits Then
            MsgBox("You don't have that many credits. Try betting less credits")
        ElseIf Gamble < Credits Then
            MsgBox("Your bet has been received. The racers are ready. Click on the yellow 'Start Race' button to begin the race.")
        Else
            MsgBox("Make sure to enter a whole number as the numerical value")
        End If

    End Sub

    Private Sub Button5_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button5.Click

        'Make the participating racers visible and keep the rest hidden.
        PictureBox1.Visible = True
        PictureBox2.Visible = True
        PictureBox3.Visible = True
        PictureBox4.Visible = True
        PictureBox5.Visible = True
        PictureBox6.Visible = False

        'Set the amount of racers into the variable.
        RacerCount = 5

        'Let the user guess who will win the race. Check for errors and then let the user know the race is ready to begin.
        WinnerPrediction = InputBox("Before the race begins, who do you think will win? Enter the name of the racer you bet on!")

        If WinnerPrediction = "Naruto" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Kakashi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Obito" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Madara" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Itachi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Sasuke" Then
            MsgBox("May the odds be ever in your favour!")
        Else
            MsgBox("Please enter one of the following: ( Naruto | Kakashi | Obito | Madara | Itachi | Sasuke )")
        End If

        'The user decides how many credits they want to bet on the race.
        Gamble = InputBox("How many credits would you like to bet?")

        If Gamble > Credits Then
            MsgBox("You don't have that many credits. Try betting less credits")
        ElseIf Gamble < Credits Then
            MsgBox("Your bet has been received. The racers are ready. Click on the yellow 'Start Race' button to begin the race.")
        Else
            MsgBox("Make sure to enter a whole number as the numerical value")
        End If

    End Sub

    Private Sub Button6_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button6.Click

        'Make the participating racers visible and keep the rest hidden.
        PictureBox1.Visible = True
        PictureBox2.Visible = True
        PictureBox3.Visible = True
        PictureBox4.Visible = True
        PictureBox5.Visible = True
        PictureBox6.Visible = True

        'Set the amount of racers into the variable.
        RacerCount = 6

        'Let the user guess who will win the race. Check for errors and then let the user know the race is ready to begin.
        WinnerPrediction = InputBox("Before the race begins, who do you think will win? Enter the name of the racer you bet on!")

        If WinnerPrediction = "Naruto" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Kakashi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Obito" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Madara" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Itachi" Then
            MsgBox("May the odds be ever in your favour!")
        ElseIf WinnerPrediction = "Sasuke" Then
            MsgBox("May the odds be ever in your favour!")
        Else
            MsgBox("Please enter one of the following: ( Naruto | Kakashi | Obito | Madara | Itachi | Sasuke )")
        End If

        'The user decides how many credits they want to bet on the race.
        Gamble = InputBox("How many credits would you like to bet?")

        If Gamble > Credits Then
            MsgBox("You don't have that many credits. Try betting less credits")
        ElseIf Gamble < Credits Then
            MsgBox("Your bet has been received. The racers are ready. Click on the yellow 'Start Race' button to begin the race.")
        Else
            MsgBox("Make sure to enter a whole number as the numerical value")
        End If

    End Sub

    Private Sub Button7_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button7.Click

        'Enable the timer to start the race and play a starting sound.
        Timer1.Enabled = True
        My.Computer.Audio.Play("C:\Users\16138\Downloads\racetothefinish.wav")

    End Sub

    Private Sub Timer1_Tick(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Timer1.Tick

        'It is randomly decided how far a racer will move every 100 milliseconds.
        Randomize()

        iRand1 = (Int(Rnd() * 25) + 1)
        iRand2 = (Int(Rnd() * 25) + 1)
        iRand3 = (Int(Rnd() * 25) + 1)
        iRand4 = (Int(Rnd() * 25) + 1)
        iRand5 = (Int(Rnd() * 25) + 1)
        iRand6 = (Int(Rnd() * 25) + 1)

        'The selected racers start the race while the others stay hidden.
        If RacerCount = 2 Then
            PictureBox1.Left = PictureBox1.Left + iRand1
            PictureBox2.Left = PictureBox2.Left + iRand2
        End If

        If RacerCount = 3 Then
            PictureBox1.Left = PictureBox1.Left + iRand1
            PictureBox2.Left = PictureBox2.Left + iRand2
            PictureBox3.Left = PictureBox3.Left + iRand3
        End If

        If RacerCount = 4 Then
            PictureBox1.Left = PictureBox1.Left + iRand1
            PictureBox2.Left = PictureBox2.Left + iRand2
            PictureBox3.Left = PictureBox3.Left + iRand3
            PictureBox4.Left = PictureBox4.Left + iRand4
        End If

        If RacerCount = 5 Then
            PictureBox1.Left = PictureBox1.Left + iRand1
            PictureBox2.Left = PictureBox2.Left + iRand2
            PictureBox3.Left = PictureBox3.Left + iRand3
            PictureBox4.Left = PictureBox4.Left + iRand4
            PictureBox5.Left = PictureBox5.Left + iRand5
        End If

        If RacerCount = 6 Then
            PictureBox1.Left = PictureBox1.Left + iRand1
            PictureBox2.Left = PictureBox2.Left + iRand2
            PictureBox3.Left = PictureBox3.Left + iRand3
            PictureBox4.Left = PictureBox4.Left + iRand4
            PictureBox5.Left = PictureBox5.Left + iRand5
            PictureBox6.Left = PictureBox6.Left + iRand6
        End If

        'The winner is declared once a racer crosses the finish line and a sound plays.
        'Once a winner is determined, the winner is compared back to the user's prediction to determine the betting results.
        'Credits are then added or reduced from the users bank balance from betting results.
        If PictureBox1.Left >= 1050 Then
            Timer1.Enabled = False
            My.Computer.Audio.Play("C:\Users\16138\Downloads\kaiba-one-winner.wav")
            MsgBox("Naruto Wins!")
            RaceWinner = "Naruto"
            NarutoWins = NarutoWins + 1
            Label2.Text = "Naruto Wins: " & NarutoWins
            If RaceWinner = WinnerPrediction Then
                MsgBox("Your guess was correct! For winning the bet, " & Gamble & " credits have been added to your bank balance.")
                Credits = Credits + Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            Else
                MsgBox("Your guess was not correct! For losing the bet, " & Gamble & " credits have been taken from your bank balance.")
                Credits = Credits - Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            End If
        ElseIf PictureBox2.Left >= 1050 Then
            Timer1.Enabled = False
            My.Computer.Audio.Play("C:\Users\16138\Downloads\kaiba-one-winner.wav")
            MsgBox("Kakashi Wins!")
            RaceWinner = "Kakashi"
            KakashiWins = KakashiWins + 1
            Label3.Text = "Kakashi Wins: " & KakashiWins
            If RaceWinner = WinnerPrediction Then
                MsgBox("Your guess was correct! For winning the bet, " & Gamble & " credits have been added to your bank balance.")
                Credits = Credits + Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            Else
                MsgBox("Your guess was not correct! For losing the bet, " & Gamble & " credits have been taken from your bank balance.")
                Credits = Credits - Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            End If
        ElseIf PictureBox3.Left >= 1050 Then
            Timer1.Enabled = False
            My.Computer.Audio.Play("C:\Users\16138\Downloads\kaiba-one-winner.wav")
            MsgBox("Obito Wins!")
            RaceWinner = "Obito"
            ObitoWins = ObitoWins + 1
            Label4.Text = "Obito Wins: " & ObitoWins
            If RaceWinner = WinnerPrediction Then
                MsgBox("Your guess was correct! For winning the bet, " & Gamble & " credits have been added to your bank balance.")
                Credits = Credits + Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            Else
                MsgBox("Your guess was not correct! For losing the bet, " & Gamble & " credits have been taken from your bank balance.")
                Credits = Credits - Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            End If
        ElseIf PictureBox4.Left >= 1050 Then
            Timer1.Enabled = False
            My.Computer.Audio.Play("C:\Users\16138\Downloads\kaiba-one-winner.wav")
            MsgBox("Madara Wins!")
            RaceWinner = "Madara"
            MadaraWins = MadaraWins + 1
            Label5.Text = "Madara Wins: " & MadaraWins
            If RaceWinner = WinnerPrediction Then
                MsgBox("Your guess was correct! For winning the bet, " & Gamble & " credits have been added to your bank balance.")
                Credits = Credits + Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            Else
                MsgBox("Your guess was not correct! For losing the bet, " & Gamble & " credits have been taken from your bank balance.")
                Credits = Credits - Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            End If
        ElseIf PictureBox5.Left >= 1050 Then
            Timer1.Enabled = False
            My.Computer.Audio.Play("C:\Users\16138\Downloads\kaiba-one-winner.wav")
            MsgBox("Itachi Wins!")
            RaceWinner = "Itachi"
            ItachiWins = ItachiWins + 1
            Label6.Text = "Itachi Wins: " & ItachiWins
            If RaceWinner = WinnerPrediction Then
                MsgBox("Your guess was correct! For winning the bet, " & Gamble & " credits have been added to your bank balance.")
                Credits = Credits + Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            Else
                MsgBox("Your guess was not correct! For losing the bet, " & Gamble & " credits have been taken from your bank balance.")
                Credits = Credits - Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            End If
        ElseIf PictureBox6.Left >= 1050 Then
            Timer1.Enabled = False
            My.Computer.Audio.Play("C:\Users\16138\Downloads\kaiba-one-winner.wav")
            MsgBox("Sasuke Wins!")
            RaceWinner = "Sasuke"
            SasukeWins = SasukeWins + 1
            Label7.Text = "Sasuke Wins: " & SasukeWins
            If RaceWinner = WinnerPrediction Then
                MsgBox("Your guess was correct! For winning the bet, " & Gamble & " credits have been added to your bank balance.")
                Credits = Credits + Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            Else
                MsgBox("Your guess was not correct! For losing the bet, " & Gamble & " credits have been taken from your bank balance.")
                Credits = Credits - Gamble
                Label1.Text = "Bank Balance: " & Credits & " Credits"
            End If
        End If

    End Sub

    Private Sub Button8_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button8.Click

        'The racers are brought back to their original starting positions and the race is reset for the user to remake or replay to their liking.
        PictureBox1.Visible = False
        PictureBox2.Visible = False
        PictureBox3.Visible = False
        PictureBox4.Visible = False
        PictureBox5.Visible = False
        PictureBox6.Visible = False

        PictureBox1.Left = 125
        PictureBox2.Left = 125
        PictureBox3.Left = 125
        PictureBox4.Left = 125
        PictureBox5.Left = 125
        PictureBox6.Left = 125

        MsgBox("The race has been reset. You can play again by clicking one of the blue buttons to select the amount of racers.")

    End Sub

    Private Sub Button9_Click_1(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button9.Click

        'Ask the user what prize they want to purchase.
        PrizeChoice = InputBox("What would you like to purchase from the shop?")

        'Check if the user has enough credits to purchase this item.
        If PrizeChoice = "Ramen Bowl" And Credits < 250 Then
            MsgBox("You do not have enough credits to purchase this item.")
        ElseIf PrizeChoice = "Shinobi Ring" And Credits < 750 Then
            MsgBox("You do not have enough credits to purchase this item.")
        ElseIf PrizeChoice = "Village Headband" And Credits < 1250 Then
            MsgBox("You do not have enough credits to purchase this item.")
        ElseIf PrizeChoice = "Hokage Cloak" And Credits < 2000 Then
            MsgBox("You do not have enough credits to purchase this item.")
        End If

        'Give the user the purchased item and subtract credits from bank balance.
        If PrizeChoice = "Ramen Bowl" And Credits >= 250 Then
            Credits = Credits - 250
            Label1.Text = "Bank Balance: " & Credits & " Credits"
            MsgBox("You have been given a bowl of ramen.")
        ElseIf PrizeChoice = "Shinobi Ring" And Credits >= 750 Then
            Credits = Credits - 750
            Label1.Text = "Bank Balance: " & Credits & " Credits"
            MsgBox("You have been given a shinobi ring.")
        ElseIf PrizeChoice = "Village Headband" And Credits >= 1250 Then
            Credits = Credits - 1250
            Label1.Text = "Bank Balance: " & Credits & " Credits"
            MsgBox("You have been given a village headband.")
        ElseIf PrizeChoice = "Hokage Cloak" And Credits >= 2000 Then
            Credits = Credits - 2000
            Label1.Text = "Bank Balance: " & Credits & " Credits"
            MsgBox("You have been given a hokage cloak.")
        End If

    End Sub
End Class




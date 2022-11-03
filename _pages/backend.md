<script>
url = "https://quotes15.p.rapidapi.com/quotes/random/"

    headers = {
        "X-RapidAPI-Key": "825200d0f8msh414d353da41bfcfp1ddcfcjsnb40ef386fce9",
        "X-RapidAPI-Host": "quotes15.p.rapidapi.com"
    }

    response = requests.request("GET", url, headers=headers)

    print(response.text)
    output = json.loads(response.text)
    return render_template("motivation.html", quotes = output)
</script>
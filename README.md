Mini-level — Inleveren
Naam: Lucas pool
Klas: SD1C
Datum: 29-10-2026
Les: GDV Les 6
________________________________________
Wat heb ik gemaakt?
Een parcour met sleutel en deur
________________________________________
Screenshot / GIF van je level
  ![alt text](../../sd/les6/galgje2/images/level.png)
________________________________________
Bewegend object
coin
// Plak hier het script of het stuk code dat het object laat bewegen.
void Update()
{
    transform.Rotate(0,0, rotateSpeed * Time.deltaTime);
}

________________________________________
Collider of trigger
...
// Plak hier de OnCollisionEnter/OnTriggerEnter code die je hebt gebruikt.
private void OnCollisionEnter(Collision other)
{
    if (other.gameObject.CompareTag("Player") && other.gameObject.GetComponent<HealthStatus>().hasKey)
    {
        Destroy(gameObject);
        GetComponent<HealthStatus>().key--;
    }
}
________________________________________
Logica met if of switch
...
// Plak hier het stuk code met jouw if- of switch-logica.
if (Input.GetKeyDown(KeyCode.Space) && stamina >= 10f && grounded == true && !isExhausted)
{
Jump();
}
________________________________________
Eigen extra idee
if (key > 0);
{
    hasKey = true;
    if (key <= 0)
        hasKey = false;
}
________________________________________
Evaluatie
Wat ging goed? en waarom?
Vloeiend de code laten clicken met elkaar
Wat vond je lastig? en waarom?
De grounded functie laten werken
Wat zou je een volgende keer anders doen?
Inplaats van : if (grounded = false)
if (!grounded) doen

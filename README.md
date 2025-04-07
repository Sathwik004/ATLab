
# 📱 AT Lab – Android Programming Snippets

## 🔔 Alert Dialog

```java
AlertDialog.Builder ab = new AlertDialog.Builder(MainActivity2.this);

ab.setTitle("Confirmation");
ab.setMessage("Do you really want to do this?");

ab.setPositiveButton("Yes", new DialogInterface.OnClickListener() {
    @Override
    public void onClick(DialogInterface dialog, int which) {
        Toast.makeText(MainActivity2.this, "Thanks!", Toast.LENGTH_SHORT).show();
    }
});

ab.setNegativeButton("No", null);
ab.show();
```

---

## 🔘 Button

```java
Button button = findViewById(R.id.button);
button.setOnClickListener((v) -> {
    // Handle button click
});
```

---

## 🍞 Toast

```java
Toast.makeText(MainActivity.this, "You clicked a button", Toast.LENGTH_SHORT).show();
```

---

## ✈️ Intent (Passing Data Between Activities)

```java
Intent intent = new Intent(MainActivity.this, MainActivity2.class);
intent.putExtra("name", "Sathwik");
intent.putExtra("age", 21);
startActivity(intent);

// In the receiving activity
String name = getIntent().getStringExtra("name");
```

---

## 🔄 Spinner (Dropdown)

```java
String[] colorss = {"Select", "Blue", "Black"};
spin = findViewById(R.id.spinner);

ArrayAdapter<String> adapter = new ArrayAdapter<>(
    this,
    android.R.layout.simple_spinner_dropdown_item,
    colorss
);
spin.setAdapter(adapter);

spin.setOnItemSelectedListener(new AdapterView.OnItemSelectedListener() {
    @Override
    public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {
        String selected = colorss[position];

        if (selected.equals("Blue")) {
            mainlayout.setBackgroundColor(Color.BLUE);
        } else if (selected.equals("Black")) {
            mainlayout.setBackgroundColor(Color.BLACK);
        } else {
            mainlayout.setBackgroundColor(Color.WHITE);
        }

        res.setLength(0);
        res.append("Selected Color: ").append(selected);
        textt.setText(res);
    }

    @Override
    public void onNothingSelected(AdapterView<?> parent) {
        mainlayout.setBackgroundColor(Color.WHITE);
    }
});
```

---

## 📋 ListView (Using the Same Adapter from Spinner)

```java
listi = findViewById(R.id.listt);
listi.setAdapter(adapter);

listi.setOnItemClickListener(new AdapterView.OnItemClickListener() {
    @Override
    public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
        String si = colorss[position];
        Toast.makeText(MainActivity.this, "Selected: " + si, Toast.LENGTH_SHORT).show();
    }
});
```

---

> ✅ This Markdown file provides neatly formatted snippets for common Android UI features using Java. Great for study notes or sharing!

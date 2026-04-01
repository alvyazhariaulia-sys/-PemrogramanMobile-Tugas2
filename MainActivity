package com.utama.tugasformregist2

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.RadioGroup
import android.widget.Toast
import androidx.activity.enableEdgeToEdge
import androidx.appcompat.app.AppCompatActivity
import androidx.core.view.ViewCompat
import androidx.core.view.WindowInsetsCompat

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContentView(R.layout.activity_register)

        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main)) { v, insets ->
            val systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars())
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom)
            insets
        }

        val etNamaLengkap = findViewById<EditText>(R.id.etNamaLengkap)
        val etEmail = findViewById<EditText>(R.id.etEmail)
        val etNomorTelepon = findViewById<EditText>(R.id.etNomorTelepon)
        val etPassword = findViewById<EditText>(R.id.etPassword)
        val etKonfirmasiPassword = findViewById<EditText>(R.id.etKonfirmasiPassword)
        val rgJenisKelamin = findViewById<RadioGroup>(R.id.rgJenisKelamin)
        val btnDaftar = findViewById<Button>(R.id.btnDaftar)

        btnDaftar.setOnClickListener {
            val nama = etNamaLengkap.text.toString().trim()
            val email = etEmail.text.toString().trim()
            val telepon = etNomorTelepon.text.toString().trim()
            val password = etPassword.text.toString().trim()
            val konfirmasiPassword = etKonfirmasiPassword.text.toString().trim()
            val selectedGenderId = rgJenisKelamin.checkedRadioButtonId

            if (nama.isEmpty() || email.isEmpty() || telepon.isEmpty() || password.isEmpty() || konfirmasiPassword.isEmpty()) {
                Toast.makeText(this, "Semua field tidak boleh kosong!", Toast.LENGTH_SHORT).show()
            } else if (selectedGenderId == -1) {
                Toast.makeText(this, "Silakan pilih jenis kelamin!", Toast.LENGTH_SHORT).show()
            } else if (password != konfirmasiPassword) {
                Toast.makeText(this, "Password dan Konfirmasi Password harus sama!", Toast.LENGTH_SHORT).show()
            } else {
                Toast.makeText(this, "Registrasi sukses!", Toast.LENGTH_LONG).show()
            }
        }
    }
}

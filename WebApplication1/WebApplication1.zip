using Microsoft.AspNetCore.Mvc;
using Microsoft.Extensions.Logging;
using System;
using System.Collections.Generic;
using System.Diagnostics;
using System.Linq;
using System.Threading.Tasks;
using WebApplication1.Models;

namespace WebApplication1.Controllers
{
	public class HomeController : Controller
	{
		private readonly ILogger<HomeController> _logger;

		public HomeController(ILogger<HomeController> logger)
		{
			_logger = logger;
		}

		public IActionResult Index()
		{
		
		
			List<Customer> customers = GetCustomers();

			return View(customers);
		}

		public IActionResult Privacy()
		{
			return View();
		}

		[ResponseCache(Duration = 0, Location = ResponseCacheLocation.None, NoStore = true)]
		public IActionResult Error()
		{
			return View(new ErrorViewModel { RequestId = Activity.Current?.Id ?? HttpContext.TraceIdentifier });
		}

		public List<Customer> GetCustomers()
		{
			List<Customer> customers = new List<Customer>
		{
				new Customer(){Id=100, Name="Jay", Dept= "Accounting"},
				new Customer(){Id=200, Name="Mark", Dept= "IT"},
					new Customer(){Id=300, Name="Srini", Dept= "Finanance"}

			//new Customer( Id100, "Jay", "Acounting"),
			//new Customer(101, "Mark", "Finanance"),
			//new Customer(102, "James", "IT")
		};

			return customers;
		}
	}
}

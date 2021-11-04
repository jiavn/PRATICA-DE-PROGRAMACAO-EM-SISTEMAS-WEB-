var myQuestions = [

	{
		question: "1 - Como se previnir da Covid19?",
		answers: {
			a: 'Lavando as mãos com agua e sabão',
			b: 'Usando mascará',
			c: 'As duas anteriores'
		},
		correctAnswer: 'c'
	},
	{
		question: "2 - Qual o melhor medicamento de prevenção para a covid19?",
		answers: {
			a: 'Cloroquina',
			b: 'Ivermectina',
			c: 'Vacina',
			d: 'Uma dose de cachaçao e limão no inicio da manha'
		},
		correctAnswer: 'c'
	},
	{
		question: "3 - Quais são os sintomas da covid19?",
		answers: {
			a: 'Todas as opções a seguir',
			b: 'Dores no corpo',
			c: 'Falta de ar',
			d: 'Febre'
		},
		correctAnswer: 'a'
	},
	{
		question: "4 - Como é transmitida a covid19?",
		answers: {
			a: 'Em contato com outra pessoa contaminada',
			b: 'Somente pelo sangue',
			c: 'Através de cães e gatos',
			d: 'Comendo manga com leite'
		},
		correctAnswer: 'a'
	},
	{
		question: "5 - O que deve ser feito caso se contamine com a Covid19?",
		answers: {
			a: 'Buscar auxílio médico e manter-se isolado',
			b: 'Ir na Farmacia e comprar rémedio',
			c: 'Prática exercicios fisicos ao ar livre',
			d: 'Se não tiver sintomas fortes, nada'
		},
		correctAnswer: 'a'
	},
	{
		question: "6 - Quem pode contrair a Covid19?",
		answers: {
			a: 'Somente idosos',
			b: 'Somentes crianças',
			c: 'Somente mulheres acima de 50 anos',
			d: 'Todas as pessoas'
		},
		correctAnswer: 'd'
	},
	{
		question: "7 - Considere a assertiva: Os jovens estão imunes da Covid19, principalmente por conta da sua alta imunidade",
		answers: {
			a: 'Certo',
			b: 'Errado',
		},
		correctAnswer: 'b'
	},
	{
		question: "8 - Qual o período correto de isolamento?",
		answers: {
			a: 'Uma semana',
			b: '5 dias',
			c: '10 dias',
			d: '14 Dias'
		},
		correctAnswer: 'd'
	},
	{
		question: "9 - Considere a assertiva: A vacina da gripe previne a Covid19",
		answers: {
			a: 'Certo',
			b: 'Errado',
		},
		correctAnswer: 'b'
	},
	{
		question: "10 - Considere a assertiva: Crianças não podem contrair o coronavírus.",
		answers: {
			a: 'Certo',
			b: 'Errado',
		},
		correctAnswer: 'b'
	}
	
	
];

var quizContainer = document.getElementById('quiz');
var resultsContainer = document.getElementById('results');
var submitButton = document.getElementById('submit');

generateQuiz(myQuestions, quizContainer, resultsContainer, submitButton);

function generateQuiz(questions, quizContainer, resultsContainer, submitButton){

	function showQuestions(questions, quizContainer){
		var output = [];
		var answers; 
		for(var i=0; i<questions.length; i++){
			
			
			answers = [];

			
			for(letter in questions[i].answers){

			
				answers.push(
					'<label>'
						+ '<input type="radio" name="question'+i+'" value="'+letter+'">'
					
						+ questions[i].answers[letter]
					+ '</label>'
				);
			}

			
			output.push(
				'<div class="question">' + questions[i].question + '</div>'
				+ '<div class="answers">' + answers.join('') + '</div>'
			);
		}

	
		quizContainer.innerHTML = output.join('');
	}


	function showResults(questions, quizContainer, resultsContainer){
			
		
		var answerContainers = quizContainer.querySelectorAll('.answers');
		
		
		var userAnswer = '';
		var numCorrect = 0;
		
		
		for(var i=0; i<questions.length; i++){

			
			userAnswer = (answerContainers[i].querySelector('input[name=question'+i+']:checked')||{}).value;
			
			
			
			if(userAnswer===questions[i].correctAnswer){
				
				numCorrect++;
				
				
				answerContainers[i].style.color = 'lightgreen';
			}
			
			else{
				
				answerContainers[i].style.color = 'red';
			}
		}

			
			resultsContainer.innerHTML = numCorrect + ' de ' + questions.length;
		}

	
	showQuestions(questions, quizContainer);

	
	submitButton.onclick = function(){
		showResults(questions, quizContainer, resultsContainer);
	}
}

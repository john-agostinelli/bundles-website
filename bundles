// Initialize particles.js
document.addEventListener('DOMContentLoaded', function() {
    if (typeof particlesJS !== 'undefined') {
        particlesJS('particles-js', {
            "particles": {
                "number": {
                    "value": 120,
"density": {
                        "enable": true,
                        "value_area": 800
                    }
                },
                "color": {
                    "value": ["#6366f1", "#10b981", "#f59e0b"]
                },
"shape": {
                    "type": "circle",
                    "stroke": {
                        "width": 0,
                        "color": "#000000"
                    },
                    "polygon": {
                        "nb_sides": 5
                    }
                },
                "opacity": {
                    "value": 0.7,
"random": false,
                    "anim": {
                        "enable": false,
                        "speed": 1,
                        "opacity_min": 0.1,
                        "sync": false
                    }
                },
                "size": {
                    "value": 3,
                    "random": true,
                    "anim": {
                        "enable": false,
                        "speed": 40,
                        "size_min": 0.1,
                        "sync": false
                    }
                },
                "line_linked": {
                    "enable": true,
                    "distance": 120,
                    "color": "#6366f1",
                    "opacity": 0.4,
                    "width": 1.5,
                    "blink": true
},
                "move": {
                    "enable": true,
                    "speed": 3,
                    "random": true,
                    "straight": false,
                    "out_mode": "bounce",
"direction": "none",
                    "random": false,
                    "straight": false,
                    "out_mode": "out",
                    "bounce": false,
                    "attract": {
                        "enable": false,
                        "rotateX": 600,
                        "rotateY": 1200
                    }
                }
            },
            "interactivity": {
                "detect_on": "canvas",
                "events": {
                "onhover": {
                    "enable": true,
                    "mode": "repulse",
                    "distance": 100
},
                    "onclick": {
                        "enable": true,
                        "mode": "push"
                    },
                    "resize": true
                },
                "modes": {
                    "grab": {
                        "distance": 140,
                        "line_linked": {
                            "opacity": 1
                        }
                    },
                    "bubble": {
                        "distance": 400,
                        "size": 40,
                        "duration": 2,
                        "opacity": 8,
                        "speed": 3
                    },
                    "repulse": {
                        "distance": 200,
                        "duration": 0.4
                    },
                    "push": {
                        "particles_nb": 4
                    },
                    "remove": {
                        "particles_nb": 2
                    }
                }
            },
            "retina_detect": true
        });
    }

    // Form submission
    document.getElementById('purchaseForm').addEventListener('submit', function(e) {
        e.preventDefault();
        const phoneNumber = document.getElementById('phoneNumber').value;
        const packageName = document.getElementById('packageName').textContent;
        const packagePrice = document.getElementById('packagePrice').textContent;
        
        // Here you would typically send this data to your backend
        // Create a more engaging purchase confirmation
        const confirmation = document.createElement('div');
        confirmation.className = 'fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-70';
        confirmation.innerHTML = `
            <div class="bg-gray-800 rounded-xl p-6 w-full max-w-md mx-4 border border-secondary-500 animate-modalIn">
                <div class="text-center">
                    <div class="w-16 h-16 bg-secondary-500/20 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i data-feather="check-circle" class="text-secondary-300 w-8 h-8"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Purchase Successful!</h3>
                    <p class="text-gray-400 mb-4">Your data package is being activated</p>
                    <div class="bg-gray-700 rounded-lg p-4 mb-6">
                        <p class="text-sm text-gray-400">Package:</p>
                        <p class="font-bold">${packageName}</p>
                        <p class="text-sm text-gray-400 mt-2">Amount:</p>
                        <p class="font-bold text-secondary-500">${packagePrice}</p>
                        <p class="text-sm text-gray-400 mt-2">Phone:</p>
                        <p class="font-bold">${phoneNumber}</p>
                    </div>
                    <button onclick="this.parentElement.parentElement.parentElement.remove()" class="w-full bg-primary-500 text-white py-3 rounded-lg font-bold hover:bg-primary-600 transition-all">
                        Awesome!
                    </button>
                </div>
            </div>
        `;
        document.body.appendChild(confirmation);
        feather.replace();
// Reset form and hide modal
        this.reset();
        hidePurchaseModal();
    });
});
// Add hover effect to package cards
document.addEventListener('DOMContentLoaded', function() {
    const packageCards = document.querySelectorAll('.bg-gray-800.rounded-xl');
    packageCards.forEach(card => {
        card.addEventListener('mouseenter', () => {
            card.style.transform = 'translateY(-8px)';
            card.style.boxShadow = '0 20px 25px -5px rgba(99, 102, 241, 0.2)';
        });
        card.addEventListener('mouseleave', () => {
            card.style.transform = 'translateY(-2px)';
            card.style.boxShadow = '0 10px 15px -3px rgba(99, 102, 241, 0.1)';
        });
    });
});

// Modal functions
function showPurchaseModal(packageName, price) {
    document.getElementById('packageName').textContent = packageName;
    document.getElementById('packagePrice').textContent = `Ksh ${price}`;
    const modal = document.getElementById('purchaseModal');
    modal.classList.remove('hidden');
    modal.style.backdropFilter = 'blur(5px)';
    document.body.style.overflow = 'hidden';
    
    // Add subtle animation to modal
    modal.querySelector('div').style.animation = 'modalIn 0.4s cubic-bezier(0.34, 1.56, 0.64, 1) forwards';
}
function hidePurchaseModal() {
    document.getElementById('purchaseModal').classList.add('hidden');
    document.body.style.overflow = 'auto';
}
